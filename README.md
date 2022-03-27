# bored-github-avatar

Periodically updates your GitHub profile avatar, based on a provided directory of images.

Uses Gravatar XML-RPC API to change your GitHub avatar, as there is no way to upload an image via the GitHub API (be patient, the syncing process between Gravatar -> GitHub usually takes some time).

The period between avatar updates is **2** hours. Already uploaded images are cached in local file `.already_uploaded_images_cache` (this is done to prevent duplicated images upload).

## Usage

Requires `Python 2(.7)` to run.

1. Make sure your GitHub account has a Gravatar profile associated and is using it.
2. If you have not defined a password for your Gravatar account yet, define it [here](https://en.gravatar.com/account/change-password/).
3. Create `.already_uploaded_images_cache` on the root of the repository (sorry, spaghetti Python code does not automatically create this file)
4. Get some images you would like to use as your GitHub avatar.
5. Run!

`python zazaza.cobrinha <email> <password> <images_dir_path>`

If you are in an Unix environment, use `screen` or `nohup` to launch script as a background process.

Example with `screen`:

`screen -dmS cobrinhahihisewiiii -- python zazaza.cobrinha <email> <password> <images_dir_path>`

## Credits

Thank you `catherine` from StackOverflow for providing boilerplate code to interact with Gravatar XML-RPC API (https://stackoverflow.com/a/26099199).