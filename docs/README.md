
```bash
brew install qemu
mkdir images
cd images
# Download the artifact from the github action
unzip images.zip
qemu-system-x86_64 \
  -kernel qemux86-64/bzImage \
  -drive file=qemux86-64/core-image-minimal-qemux86-64.ext4 \
  -append 'root=/dev/sda rw console=ttyS0' \
  -nographic
```

