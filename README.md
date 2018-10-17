# Dipstick Dataset

    POWERED BY
    ▀█▀ ▒█▄░▒█ ▒█░▄▀ ▒█▀▀█ ▒█▀▀▀ ▒█▀▄▀█ ▒█▀▀▀ ▒█▄░▒█ ▀▀█▀▀ ░█▀▀█ ▒█░░░
    ▒█░ ▒█▒█▒█ ▒█▀▄░ ▒█▄▄▀ ▒█▀▀▀ ▒█▒█▒█ ▒█▀▀▀ ▒█▒█▒█ ░▒█░░ ▒█▄▄█ ▒█░░░
    ▄█▄ ▒█░░▀█ ▒█░▒█ ▒█░▒█ ▒█▄▄▄ ▒█░░▒█ ▒█▄▄▄ ▒█░░▀█ ░▒█░░ ▒█░▒█ ▒█▄▄█
    https://www.inkremental.co/

The images are of minimum 512 pixels and maximum 1024 pixels of withd or height, in some images it is obfuscated with black patches, because there were too many very small rods.

![VOC_dipstick/JPEGImages/train_image44.jpg](/home/inkremental-3/gitKraken/dipstick/VOC_dipstick/JPEGImages/train_image44.jpg)

## VOC format

See more [https://pjreddie.com/projects/pascal-voc-dataset-mirror/](https://pjreddie.com/projects/pascal-voc-dataset-mirror/)

## make sets

``` bash
# Comand to make sets
cd VOC_dipstick/Annotations
ArrayName=(train_*)
for var in "${ArrayName[@]}"
do
echo "${var/\.xml/}" >> ../ImageSets/Main/train.txt
done

ArrayName=(*)
for var in "${ArrayName[@]}"
do
echo "${var/\.xml/}" >> ../ImageSets/Main/valid.txt
done

```