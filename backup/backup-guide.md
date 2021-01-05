# Backup Guide

It's likely that your projects are already backed up to GitHub or some similar hosting service. However, the code itself does not suffice for a complete backup. You might need to take a copy of environmental variables, SSH keys, settings, files and more.

The following guide is not meant to be exhaustive, but acts as a starting point for organizing the backup process. Note you will need to replace `$volume` with the actual name of your backup volume.

### Backup application list

List the currently installed applications on your system and store them on a `txt` file.

```bash
ls -l /Applications/ > /$volume/applications.txt
```

### SSH Keys

##### Backup SSH Keys

```bash
cp -r ~/.ssh /$volume/
```

##### Restore SSH Keys

```bash
cp -r /$volume/.ssh ~/
```

### PGP Keys

##### Backup PGP Keys

```bash
gpg --armor --export > /$volume/pgp-public-keys.asc
gpg --armor --export-secret-keys > /$volume/pgp-secret-keys.asc
gpg --armor --export-ownertrust > /$volume/pgp-ownertrust.asc
```

##### Restore PGP Keys

```bash
gpg --import /$volume/pgp-public-keys.asc
gpg --import /$volume/pgp-private-keys.asc
gpg --import-ownertrust /$volume/pgp-ownertrust.asc
```

### Environmental variables

##### Backup env variable files from workspace directory

```bash
cd $workspaceDir
find . -iname '*.env' -exec rsync -R "{}" /$volume/Workspace \;
```

##### Restore env variable files

```bash
rsync -R /$volume/Workspace $workspaceDir;
```

### Bash profile

##### Backup bash profile

```bash
cp ~/.bash_profile /$volume/
```

##### Restore bash profile

```bash
cp /$volume/.bash_profile ~/
```

### npm settings

##### Backup npm settings

```bash
cp ~/.npmrc /$volume/
```

##### Restore npm settings

```bash
cp /$volume/.npmrc ~/
```

### Git Config

##### Backup git config

```bash
cp ~/.gitconfig /$volume/
```

##### Restore git config

```bash
cp /$volume/.gitconfig ~/
```

### KeePassXC

##### Backup KeePassXC database and key file

- Backup the external key file (if any)

  ```bash
  cp ~/keepass.key /$volume/
  ```

- Backup the kdbx database itself.

  ```bash
  cp ~/keepass.kdbx /$volume/
  ```

##### Restore KeePassXC database and key file

Simply restore the files to a directory of preference and locate them via the KeePassXC app.

### Browser bookmarks

Use the browser interface to backup/restore your bookmarks.

### Brew

##### Backup homebrew packages

```bash
brew bundle dump --file /$volume/homebrew-dump
```

##### Restore homebrew packages

```bash
brew bundle install --file /$volume/homebrew-dump
```
