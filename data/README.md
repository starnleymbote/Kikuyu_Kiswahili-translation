> python preprocess.py -train_src data/src-train.txt -train_tgt data/tgt-train.txt -valid_src data/src-val.txt -valid_tgt data/tgt-val.txt -save_data data/data -src_vocab_size 1000 -tgt_vocab_size 1000

> python train.py -data data/data -save_model /n/rush_lab/data/tmp_ -gpuid 0 -rnn_size 100 -word_vec_size 50 -layers 1 -train_steps 100 -optim adam  -learning_rate 0.001

//////////////////////////////////////////////////////////////////////////
 python train.py -data data2/data2 -save_model data/kikuyu_kiswahili -gpuid 0 -rnn_size 100 -word_vec_size 50 -layers 1 -train_steps 100 -optim adam  -learning_rate 0.001



************************************************************************
python train.py -data data2/data -save_model kikuyu_kiswahili_model -gpuid 0 -rnn_size 100 -word_vec_size 50 -layers 1

____________________ python preprocess.py -train_src data20/kikuyu-src-data.txt -train_tgt data20/kiswahili-src-data.txt -valid_src data20/kikuyu-val.txt -valid_tgt data20/kiswahili-val.txt -save_data data20/demo -src_vocab_size 300 -tgt_vocab_size 30_________

TESTING FOR ACCURACY LEVEL ;; https://github.com/OpenNMT/OpenNMT/issues/290


checkout ;; opts.py ::change the number of default steps for every logging

testing the demo model ;;python translate.py -model data/kikuyu_kiswahili_model_step_31520.pt -src data/kiuk.txt -output pred2.txt -replace_unk -verbose


 python translate.py -model data/kikuyu_kiswahili_model_nm_step_100000.pt -src data/kiuk.txt -output data/pred.txt -replace_unk -verbose

 ;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
 WELL TRANSLATED WORDS
 ;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;

 Mwathani
 Niinge Ngai akiuga atire .
 Agiita mutamburuko ucio 
 Nyoka ĩkĩĩra mũtumia atĩrĩ
 Ngai akiuga , nikugie utheri , gugikia utheri .
 Ngai akiona ati utheri ni mwega , akigeyania utheri na nduma .
 Utheri akiwita muthenya nayo nduma akimiita utuku . Nakuo gugituka , gugicooka gugikia . Ucio niguo wari muthenya wa mbere .
 Mũgũnda gatagatĩ ,
Nyoka ĩkĩĩra mũtumia atĩrĩ .
Nĩ maheeni , mũtingĩkua .
Maitho maanyu nĩmakũhingũka , 
Nyoka akiira mutumia
arĩa anene .
--------------------------------------------------------------------------------
Rĩrĩa Herode aamenyire
Rĩrĩa , aamenyire
---------------------------------------------------------------------------------
mũhaane ta Ngai .
Enoku aarĩ ithe wa Iradu
naake Methushaeli aarĩ ithe wa Lameki .
Lameki aahikirie atumia eerĩ ; 