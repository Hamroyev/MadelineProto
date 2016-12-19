## Method: channels\_updatePinnedMessage  

### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|silent|[Bool](../types/Bool.md) | Optional|
|channel|[InputChannel](../types/InputChannel.md) | Required|
|id|[int](../types/int.md) | Required|


### Return type: [Updates](../types/Updates.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) {
    $this->bot_login($token);
}
if (isset($number)) {
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$Updates = $MadelineProto->channels_updatePinnedMessage(['silent' => Bool, 'channel' => InputChannel, 'id' => int, ]);
```