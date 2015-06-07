# Passphrase in Keychain

SSH Agent can store passphrases to keys in the login keychain. This way
you dont have to remember to load your key each time you restart your
machine

```
ssh-add -K
ssh-add -K path/to/private_key
```

Source: [blog post].

[blog post]: http://fplanque.com/dev/mac/secure-ssh-private-keys-on-mac-osx-10-5
