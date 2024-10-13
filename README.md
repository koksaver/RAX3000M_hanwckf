Quickstart
Run git clone --depth=1 https://github.com/hanwckf/immortalwrt-mt798x.git to clone the source code.

Run cd immortalwrt-mt798x to enter source directory.

Run ./scripts/feeds update -a to obtain all the latest package definitions defined in feeds.conf / feeds.conf.default

Run ./scripts/feeds install -a to install symlinks for all obtained packages into package/feeds/

Copy the configuration file for your device from the defconfig directory to the project root directory and rename it .config

# MT7981
cp -f defconfig/mt7981-ax3000.config .config

# MT7986
cp -f defconfig/mt7986-ax6000.config .config

# MT7986 256M Low Memory
cp -f defconfig/mt7986-ax6000-256m.config .config
Run make menuconfig to select your preferred configuration for the toolchain, target system & firmware packages.

Run make -j$(nproc) to build your firmware. This will download all sources, build the cross-compile toolchain and then cross-compile the GNU/Linux kernel & all chosen applications for your target system.

## Tips

- It may take a long time to create a `.config` file and build the OpenWrt firmware. Thus, before create repository to build your own firmware, you may check out if others have already built it which meet your needs by simply [search `Actions-Openwrt` in GitHub](https://github.com/search?q=Actions-openwrt).
- Add some meta info of your built firmware (such as firmware architecture and installed packages) to your repository introduction, this will save others' time.

## Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cowtransfer](https://cowtransfer.com)
- [WeTransfer](https://wetransfer.com/)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [ActionsRML/delete-workflow-runs](https://github.com/ActionsRML/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)

## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
