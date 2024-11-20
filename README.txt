Integrantes:
    Debernardi Álvaro       42.890.685
    Dellafiore León Lucas   39.546.206

CPU Sim version: 
    3.9.0

Registros added:

    si          Source direction
    di          Destination direction
    mdr8        8-bit Manipulation

Instructions added:

    loadsrc     Store Address in si
    loaddest    Store Address in di
    strcpy      Copy String from src to dest

Microinstructions added:

    Memory Access:
        mdr8->Main[mar]
        Main[mar]->mdr8

    Increment:
        Inc1-si 
        Inc1-di
        Dec2-pc
        Dec1-acc

    TransferRTR:
        di->mar
        si->mar
        mar->di
        mar->si

    Test:
        if(acc==0)skip-1

