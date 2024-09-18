# hic-eventgen

Stripped down version of the [hic-eventgen code](https://github.com/Duke-QCD/hic-eventgen), used only to generate an EOS

# SMASH particle list vs UrQMD particle list
There are separate Git branches for the SMASH particle list and the UrQMD particle list. Please select the one you want.

# Installation
```
git clone --recursive --recurse-submodules --branch urqmd https://github.com/j-f-paquet/eos_maker.git eos_maker_urqmd

cd eos_maker_urqmd

python3 -m venv --system-site-packages --without-pip .
source bin/activate

bash local/install  # To install the `frzout` package
```

# Usage

## For production

```
python3 eos.py --res-width-off --species=urqmd --Tmax 1.0 --write-bin eos_urqmd.bin --music_output_format
```

## Just to see the output

```
python3 eos.py --res-width-off --species=urqmd --Tmax 1.0
```
