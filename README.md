# TicTacToe Flatpak

A very fun Tetris-like game!

To know more refer: https://github.com/sugarlabs/block-party-activity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.BlockPartyActivity.git
cd org.sugarlabs.BlockPartyActivity
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.BlockPartyActivity.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.BlockPartyActivity
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.BlockPartyActivity.json
```
