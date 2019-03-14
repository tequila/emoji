# Tequila Emoji

This library provides simple facade class to detect emoji in text.
At the moment, library is able to detect all emoji, including added in Unicode 11.
Regular expression is taken from [Adam Merrifield's answer on Stack Overflow](https://stackoverflow.com/a/20208095)
and is slightly modified to detect emoji with skin tones.

## Installation
The library should be installed by Composer:

```bash
composer require tequila/emoji
```

## Usage

```php
<?php

use Tequila\Emoji\Emoji;

$text = 'This string contains emojis: 😎 😍 😘👊🏿 ✊🏿 🤛🏿';

// Check if text contains emoji
$textContainsEmoji = Emoji::presentInText($text);

// Detect all emoji in text
$detectedEmoji = Emoji::detectInText($text); // ['😎', '😍', '😘', '👊🏿', '✊🏿', '🤛🏿']
```

## Support

If you need additional functionality - feel free to create an issue.