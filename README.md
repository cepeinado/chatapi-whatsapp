# Client for WhatsApp API (by Chat API)


This package makes it easy to send WhatsApp messages using [Chat API](https://chat-api.com/) with php.

## Contents

- [Installation](#installation)
- [Usage](#usage)
    - [Available Message methods](#available-message-methods)

## Installation

You can install the package via composer:

``` bash
composer require cepeinado/chatapi-whatsapp
```

## Usage

``` php
use ChatAPI\ChatAPIMessage;

ChatAPIMessage::create()
    ->to($phone) // your user phone
    ->file('/path/to/file','My Photo.jpg')
    ->content('Your invoice has been paid');
```

### Available Message methods

- `to($phone)`: (integer) Recipient's phone.
- `content('message')`: (string) Message.
- `file('/path/to/file','My Photo.jpg')`: (string) File real path, you can also send the file contents and pass two additional params for file name and file mime type (required)
- `file('/path/to/file','My Photo.jpg','image/jpg')`
