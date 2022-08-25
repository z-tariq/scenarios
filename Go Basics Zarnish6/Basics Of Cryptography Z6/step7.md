---
title: Cryptography Example
---

{{copy filename='code.go'}}

```go
package main

import (
	"crypto/aes"
	"encoding/hex"
	"fmt"
)

func encryptMessage(key string, message string) string {
	c, err := aes.NewCipher([]byte(key))
	if err != nil {
		fmt.Println(err)
	}
	msgByte := make([]byte, len(message))
	c.Encrypt(msgByte, []byte(message))
	return hex.EncodeToString(msgByte)
}

func decryptMessage(key string, message string) string {
	txt, _ := hex.DecodeString(message)
	c, err := aes.NewCipher([]byte(key))
	if err != nil {
		fmt.Println(err)
	}
	msgByte := make([]byte, len(txt))
	c.Decrypt(msgByte, []byte(txt))

	msg := string(msgByte[:])
	return msg
}

func main() {

	plainText := "This is a secret"
	key := "this_must_be_of_32_byte_length!!"

	emsg := encryptMessage(key, plainText)
	dmesg := decryptMessage(key, emsg)

	fmt.Println("Encrypted Message: ", emsg)
	fmt.Println("Decrypted Message: ", dmesg)
}

```
{{ /copy }}

Running this code in your integrated development environment will produce the following output:

Encrypted Message:  319d4fa655ed543b4aa0d1efdc3619d8
Decrypted Message:  This is a secret

Lets run this code

{{ execute }}
```
go run code.go
```
{{ /execute }}
