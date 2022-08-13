# ENUNU Multisinger Model (Japanese)
Japanese multisinger model (mixed singers model) used for ENUNU model pretraining.

The data used for training this will **NOT** be shared to the public.

This model is using the HED and dictionary provided by [UPT3] to give a variety of flags to the user.

## Training settings

Conv1DResNet (flagged version):
>* Timelag: FFN, 64 hidden_dim, 4 layers.
>* Duration: LSTMRNN, 64 hidden_dim, 4 layers.
>* Acoustics: Conv1dResnet, 256 hidden_dim, 6 layers.

Conv1DResNet (flagless version):
>* Timelag: FFN, 64 hidden_dim, 4 layers.
>* Duration: LSTMRNN, 64 hidden_dim, 4 layers.
>* Acoustics: Conv1dResnet, 256 hidden_dim, 6 layers.

Conv1DResNet + Diff-based vibrato (flagged version):
>* Timelag: MDNv2, 32 hidden_dim, 3 layers.
>* Duration: MDNv2, 256 hidden_dim, 3 layers.
>* Acoustics: Conv1dResnet, 256 hidden_dim, 6 layers.

Conv1DResNet + Diff-based vibrato (flagless version):
>* Timelag: MDNv2, 32 hidden_dim, 3 layers.
>* Duration: MDNv2, 256 hidden_dim, 3 layers.
>* Acoustics: Conv1dResnet, 256 hidden_dim, 6 layers.

Conv1DResNet + Diff-based vibrato (flagged test version):
>* Timelag: MDNv2, 32 hidden_dim, 3 layers.
>* Duration: MDNv2, 256 hidden_dim, 3 layers.
>* Acoustics: Conv1dResnet, 512 hidden_dim, 6 layers.

## Difference between flagged version and flagless version
The differences are that the flagged version is better suited to model that contains flags for extra vocal types, while flagless is intended for models that are flagless or contains no extra vocal types in the database.

## How to use
To use this model for pretrained model, point to the folder inside the exp folder

Example: `{model_name}/exp/unnamed_CeVOX_Cantano_Al_Kit`

## Disclaimer
* Please note that you may NOT use this model in circumstances other than pretraining for NNSVS (You shouldn't anyway, as the databases used are not at their full length).
* Please follow the instructions in the README.txt file if you wish to release a public model using this pretrained model.
* You might not want to pretrain the timelag and duration models using the default settings if you are using the MDN model type for duration and timelag. It seems that this breaks training.

## Special thanks
Special thanks to UtaUtaUtau, PixPrucer, xuu, ryu, カノン, ちかの, and PumpkinVA for providing and agreeing to contribute their singing databases into this model, along with Nekro for providing Colab Pro to train on.

[UPT3]: https://github.com/UPT3/nnsvs-japnese-plus
