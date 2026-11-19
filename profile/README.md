<div align="center">

# Open Mapple

**The best implementation of iOS on Android hardware.**

[Website](https://open-mapple.pages.dev) · [Install](https://open-mapple.pages.dev/install) · [Devices](https://open-mapple.pages.dev/devices) · [Docs](https://open-mapple.pages.dev/docs) · [FAQ](https://open-mapple.pages.dev/faq)

</div>

Open Mapple runs Apple's open-source XNU kernel on Android phones, with our own patches and drivers for their real
hardware: GPU, display, touch, Wi-Fi, Bluetooth, sound and sensors. iOS comes from Apple to your own computer, and we
never patch its binaries. It builds like a custom ROM.

> **Release 1 is out** (18 November 2026): iOS 16.7.16 on the realme 8i.
> [Download](https://github.com/open-mapple/mapple_releases/releases/tag/spaced-1.0) · [Install guide](https://open-mapple.pages.dev/install)

## Why it's different

|  |  |
| --- | --- |
| **Fixed in the kernel** | Real drivers for the phone's hardware, so iOS sees devices it already understands. |
| **iOS binaries unpatched** | Apple's binaries as Apple ships them. Our drivers, and a few small fixes, most off by default. |
| **Built like a ROM** | One manifest, one build command, reproducible releases. Nothing of Apple's in our repos. |

## Devices

| Phone | SoC | Status |
| --- | --- | --- |
| realme 8i (`spaced`) | MediaTek Helio G96 (MT6781) | Supported: release 1, iOS 16.7.16 |
| Redmi Note 10 Pro (`sweet`) | Qualcomm SM7150 | Build only, maintainer wanted |
| Pixel 4a (`sunfish`) | Qualcomm SM7150 | Build only, maintainer wanted |

What works on each phone is on its [device page](https://open-mapple.pages.dev/devices).

## Part of every install

- **Mapple**: the control centre on the phone. See what the hardware is doing, change how the phone starts,
  sideload apps from IPA files and turn on optional tweaks. Safe mode brings the phone back with its defaults.
- **SplitBoot**: keeps Android and puts iOS beside it, with a boot menu at every start.

## Repositories

| Area | Repositories |
| --- | --- |
| Start here | [`manifest`](https://github.com/open-mapple/manifest): the repo manifest that checks out everything below |
| Kernel | [`xnu_kernel_mediatek_common`](https://github.com/open-mapple/xnu_kernel_mediatek_common), [`xnu_kernel_mediatek_mt6781`](https://github.com/open-mapple/xnu_kernel_mediatek_mt6781), [`xnu_kernel_qcom_common`](https://github.com/open-mapple/xnu_kernel_qcom_common) |
| Devices | [`xnu_device_realme_spaced`](https://github.com/open-mapple/xnu_device_realme_spaced), [`xnu_device_xiaomi_sweet`](https://github.com/open-mapple/xnu_device_xiaomi_sweet), [`xnu_device_google_sunfish`](https://github.com/open-mapple/xnu_device_google_sunfish) |
| Boot | [`mapple_loader`](https://github.com/open-mapple/mapple_loader), [`mapple_splitboot`](https://github.com/open-mapple/mapple_splitboot) |
| Graphics | [`mapple_gpu_mali`](https://github.com/open-mapple/mapple_gpu_mali), [`mapple_gpu_adreno`](https://github.com/open-mapple/mapple_gpu_adreno) |
| User space | [`mapple_userland`](https://github.com/open-mapple/mapple_userland) |
| Build and release | [`mapple_build`](https://github.com/open-mapple/mapple_build), [`mapple_vendor`](https://github.com/open-mapple/mapple_vendor), [`mapple_releases`](https://github.com/open-mapple/mapple_releases) |

Mapple (the control centre) and the release assembler are closed source.

## Get started

- **Install** a release on a supported phone: [install guide](https://open-mapple.pages.dev/install). The release is
  assembled from your own iOS download on Windows, Linux or macOS.
- **Build** from source on a Mac with `envsetup`, `lunch` and `mka`: [build guide](https://open-mapple.pages.dev/build).
- **Port** a new phone: [porting guide](https://open-mapple.pages.dev/docs/guides/porting).

## Ground rules

- Nothing of Apple's or a phone vendor's goes into any repository: no IPSW, images, firmware or device dumps.
- Apple ID, iCloud and the App Store are out of scope. FairPlay-encrypted apps are not supported.
- Every hardware change sits behind a boot argument, and safe boot is always the way back.

## Credits and legal

Open Mapple builds on the work of the projects and people listed on the
[credits page](https://open-mapple.pages.dev/credits). Each repository carries its own licence.

Open Mapple is an independent research project, not affiliated with or endorsed by Apple Inc., MediaTek, Qualcomm,
realme, Xiaomi or Google. Apple, iOS, iPhone and Metal are trademarks of Apple Inc., registered in the U.S. and other
countries. Other names are trademarks of their respective owners.

## Use of AI

Open Mapple is developed by one person, which would not be possible without help, so AI tools were used for
research, code and documentation. Every change was reviewed by a person before it landed, and AI filler was removed
wherever we found it. If something still reads that way, please open an issue.

<div align="center">

Maintained by [Pritish Joshi](https://pritish.eu) ([@DrtSinX98](https://github.com/DrtSinX98))

</div>
