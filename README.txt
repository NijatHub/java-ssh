This file contains succesful progress during the lesson:

	1.Open git bash
	2.Generate ssh key:
		ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
	3.Choose the file location:
		Enter file in which to save the key (/home/your_user/.ssh/id_rsa):
	4.Set a Passphrase (Optional but Recommended):
		Enter passphrase (empty for no passphrase):
	5.Add the SSH Key to the SSH Agent:
		5.1.eval "$(ssh-agent -s)"
		5.2.ssh-add ~/.ssh/id_rsa
	6.Copy the Public Key:
		cat ~/.ssh/id_rsa.pub
	7.Add the SSH Key to GitHub:
		7.1.Go to GitHub → Settings → SSH and GPG keys.
		7.2.Click "New SSH Key".
		7.3.Paste the copied SSH key and save it.
	7.Test the Connection:
		ssh -T git@github.com
	If successful, you'll see:
		Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.
	9.Push changes using SSH:
		9.1.cd your-repo
		9.2.git add .
		9.3.git commit -m "Initial commit"
		9.4.git push origin main
