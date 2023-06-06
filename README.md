# ghw-gpg
Prove yourself with GPG

Intro to GPG:
What is it?

What can it do?

What are some real world use cases?

<img width="740" alt="Screenshot 2023-06-06 at 10 16 50 AM" src="https://github.com/Emmarie-Ahtunan/ghw-gpg/assets/86572370/10cb69be-25cf-4cf8-8c41-0658e12332d3">

Slide from Wei's stream.


Get your GPG Key:

1. Fork repo: ```Fork https://github.com/wei/ghw-gpg on GitHub```

2. Generate a GPG Key: ```$ gpg --gen-key```

3. Find your key: ```$ gpg --list-secret-keys --keyid-format=long```

4. Upload your key to a key server: ```$ gpg --send-keys <KEY ID>```

5. Download my public key:  ```$ gpg --search-keys "email@gmail.com"```

6. List all locally stored keys (key should be visible): ```$ gpg --list-keys```

7. Create a hot-take.txt and input a hot take.

8. Sign your hot take .txt file: ```$ gpg --sign --armor hot-take.txt```

9. Open hot-take.txt.asc file and post the contents on https://github.com/wei/ghw-gpg/issues/1

10. To read hot takes, put the signed message into a file and run this: ```$ gpg --decrypt <FILE NAME>```

11. Encrypt your hot take txt file for a specific recipient: ```$ gpg --encrypt --armor \--recipient email@gmail.com hot-take.txt```

12. The recipient(s) will be the only one who can decrypt the file: ```$ gpg --decrypt <FILE NAME>```

13. Impersonate Another GitHub User: ```$ GIT_COMMITTER_NAME="Wei" GIT_COMMITTER_EMAIL="weionstream@gmail.com" \git commit --author="Wei <weionstream@gmail.com>" -m "Your Commit Message"```

# Signing Git Commits:

14. Retrieve your Key ID: ```$ gpg --list-secret-keys --keyid-format=long```

15. Export your public key:```$ gpg --armor --export <KEY_ID>```
      Save it under GitHub Settings: SSH and GPG keys > New GPG Key

16. Tell Git about your Key: ```$ git config --global user.signingkey <KEY_ID>```

17. Sign your Git Commits: ```$ git commit -S -m "YOUR_COMMIT_MESSAGE"```

18. Automatically sign all commits: ```$ git config --global commit.gpgsign true```


For more information visit: https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key
