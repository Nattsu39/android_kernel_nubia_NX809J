# NX809J prebuilt kernel and display UAPI

`prebuilt/Image` is the verified personal **6.12.38 / ReSukiSU** build from
`Nattsu39/OnePlus_KernelSU_SUSFS`, branch `nx809j-resukisu-real-38`.
Its `OP-WILD` version suffix is retained from that build.

Exact source revisions, the successful Actions run, SHA256, ABI requirements and
camera GPIO pairing are recorded in `prebuilt/kernel-provenance.json`.
Only run 37102828355 is used: the earlier build omitted the stable GKI ABI mode
and is incompatible with the retained stock drivers.

The ROM builds a fresh boot image around this Image. DTB, the reviewed DTBO with
shared camera GPIOs 533/536, display UAPI and stock driver inputs are retained.
`Image.stock-gki-bak` is historical and is not a build input.

This prebuilt does not change the ROM build variant or APK/APEX signing keys.
ReSukiSU remains part of the kernel when the Android userspace is built as user.
