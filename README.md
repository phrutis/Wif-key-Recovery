# Wif-key-Recovery v1.0
Programs GPU and CPU for restoring part (end) of a WIF private key</br>
This is a modified version of [Rotor-Cuda](https://github.com/phrutis/Rotor-Cuda) recovers missing characters for key from address(es) bitcoin and ethereum and public key(s)</br>
Fast speed and ease of use will ease your recovery WIF private key from paper wallet. </br>
Multiple GPU cards can be used for large end key</br>
To restore the middle of the key, use [**WifSolverCuda**](https://github.com/phrutis/WifSolverCuda)</br>

### Example GPU
Finding part of the Compressed WIF private key on the GPU

Run ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5q2knEYhh8QqUvneZ6WMcYzAgU -m address --coin BTC 1ByGDsGaosE24BLK2eHfxFPP2DRZTrPrGU```

![GPUK](https://user-images.githubusercontent.com/82582647/163684345-66d56bc4-5ff0-468b-8ff8-f5cbfebba5ad.png)

### Example GPU
Finding part of the Uncompressed WIF private key on the GPU

Run ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif 5HpJKti5tJQz1FEbqSCgMYkNG4cJ94CDYQTjQVR -m address --coin BTC 1BoXY7jyusWuPrvTQc4BVyBP1JVyYhZcCM```

![gpu5](https://user-images.githubusercontent.com/82582647/163684406-87e85a3a-abc2-4510-8bd9-edb70af46eb3.png)

### Example CPU
Finding part of the Compressed WIF private key on the CPU

Run ```Rotor-Cuda.exe -t 6 -wif KwDmUPELZRrrc5q2knEYhh8QqUvneZ6WMcYzAgUe -m address --coin BTC 1ByGDsGaosE24BLK2eHfxFPP2DRZTrPrGU```

![cpuk](https://user-images.githubusercontent.com/82582647/163684483-142a558d-26c6-4829-85cf-29a25cdb74e7.png)

### Example CPU
Finding part of the Uncompressed WIF private key on the CPU

Run ```Rotor-Cuda.exe -t 6 -wif 5HpJKti5tJQz1FEbqSCgMYkNG4cJ94CDYQTjQVRq -m address --coin BTC 1BoXY7jyusWuPrvTQc4BVyBP1JVyYhZcCM```

![cpu5](https://user-images.githubusercontent.com/82582647/163684498-833fe49e-44e0-4695-9ec7-d4261d8a2a07.png)

## Other options
CPU Bitcoin Multi Address mode:</br>
Run: ```Rotor-Cuda.exe -t 1 -wif KwDmUPELZRrrc5q -m addresses --coin BTC  -i BASE.bin```

CPU Bitcoin Single Addres mode:</br>
Run:  ```Rotor-Cuda.exe -t 1 -wif KwDmUPELZRrrc5 -m address --coin BTC 1PWCx5fovoEaoBowAvF5k91m2Xat9bMgwb```

CPU ETHEREUM Multi Address mode:</br>
Run: ```Rotor-Cuda.exe -t 1 -wif KwDmUPELZRrrc5q -m addresses --coin eth -i addresses_eth_sorted.bin```

CPU ETHEREUM Single Addres mode:</br>
Run: ```Rotor-Cuda.exe -t 1 -wif KwDmUPELZRrrc5q2knEYh -m address --coin eth 0xfda5c442e76a95f96c09782f1a15d3b58e32404f```

CPU Public keys Multi X Points mode:</br>
Run: ```Rotor-Cuda.exe -t 1 -wif KwDmUPELZRrrc5q2k -m xpoints --coin BTC -i xpoints_sorted.bin```

CPU Public key Single X Point mode:</br>
Run: ```Rotor-Cuda.exe -t 1 -wif KwDmUPE -m xpoint --coin BTC a2efa402fd5268400c77c20e574ba86409ededee7c4020e4b9f0edbee53de0d4```

GPU Bitcoin Multi Address mode:</br>
Run: ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5q -m addresses --coin BTC -i hash160_out_sorted.bin```

GPU Bitcoin Single Addres mode:</br>
Run: ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5q2k -m address --coin BTC 1PWCx5fovoEaoBowAvF5k91m2Xat9bMgwb```

GPU ETHEREUM Multi Address mode:</br>
Run: ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5 -m addresses --coin eth -i addresses_eth_sorted.bin```

GPU ETHEREUM Single Addres mode:</br>
Run:```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZR-m address --coin eth 0xfda5c442e76a95f96c09782f1a15d3b58e32404f```

GPU Public key Multi X Points mode:</br>
Run: ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5q2k -m xpoints --coin BTC -i xpoints_sorted.bin```

GPU Public key Single X Point mode:</br>
Run: ```Rotor-Cuda.exe -t 0 -g --gpui 0 --gpux 256,256 -wif KwDmUPELZRrrc5q2k -m xpoint --coin BTC ceb6cbbcdbdf5ef7150682150f4ce2c6f4807b349827dcdbdd1f2efa885a2630```</br>

For Multi GPU use:</br>
Run 8 GPUs: ```Rotor-Cuda.exe -t 0 -g --gpui 0,1,2,3,4,5,6,7 --gpux 256,256,256,256,256,256,256,256,256,256,256,256,256,256,256,256 -wif KwDmUPELZRrrc5q2knEYhh8QqUvneZ6WMcYz -m address --coin BTC 1ByGDsGaosE24BLK2eHfxFPP2DRZTrPrGU```

- [**How to create databases**](https://github.com/phrutis/Rotor-Cuda/blob/main/Others/) and [**additional parameters**](https://github.com/phrutis/Rotor-Cuda/blob/main/Others/Help.md)

## Building
### Windows
- Microsoft Visual Studio Community 2019
- CUDA version [**10.22**](https://developer.nvidia.com/cuda-10.2-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork)
## License
- Rotor-Cuda is licensed under GPLv3.

## Donation
- BTC: bc1qh2mvnf5fujg93mwl8pe688yucaw9sflmwsukz9

## __Disclaimer__
ALL THE CODES, PROGRAM AND INFORMATION ARE FOR EDUCATIONAL PURPOSES ONLY. USE IT AT YOUR OWN RISK. THE DEVELOPER WILL NOT BE RESPONSIBLE FOR ANY LOSS, DAMAGE OR CLAIM ARISING FROM USING THIS PROGRAM.
