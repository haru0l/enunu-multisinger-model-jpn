# enunu-multimodel-jpn
Japanese multisinger model (mixed singers model) used for ENUNU model pretraining

The data used for training this will NOT be shared to the public.

This model is using the HED and dictionary provided by DYVAUX to give a variety of flags to the user.

The settings used are as follows:

v1.0:
Timelag: FFN, 64 hidden_dim, 4 layers.
Duration: LSTMRNN, 64 hidden_dim, 4 layers.
Acoustics: Conv1dResnet, 256 hidden_dim, 6 layers.

To use this model for pretrained model, point to the folder inside the exp folder.

Please note that you may NOT use this model in circumstances other than pretraining for NNSVS (You shouldn't anyway, as the databases used are not at their full length).

Special thanks to UtaUtaUtau, PixPrucer, xuu, ryu, カノン, ちかの, and PumpkinVA for providing and agreeing to contribute their singing databases into this model, along with Nekro for providing Colab Pro to train on.

Please follow the instructions in the README.txt file if you wish to release a public model using this pretrained model.
