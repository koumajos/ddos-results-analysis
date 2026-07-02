# Best Hyperparameters by Model and Configuration

Extracted most frequently chosen hyperparameters across 4 sets and multiple runs.

## CNN

### Globally Best Parameters (Identical across all setups)
- `batch_size`: **128**
- `dropout`: **0.3015326907011207**
- `filters`: **16**
- `kernel_size`: **3**
- `learning_rate`: **0.0015316887092832183**
- `num_conv_layers`: **2**

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | m | r | *(same as global)* |

---

## GRU

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `batch_size`: 128<br>`bidirectional`: 0<br>`dropout`: 0.3582262872931279<br>`hidden_size`: 232<br>`learning_rate`: 0.0018380129273019813<br>`num_layers`: 2 |
| seq | b | r | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.3201193842329457<br>`hidden_size`: 164<br>`learning_rate`: 0.00013834563572216358<br>`num_layers`: 4 |
| seq | b | rsd | `batch_size`: 32<br>`bidirectional`: 0<br>`dropout`: 0.0241111147760225<br>`hidden_size`: 253<br>`learning_rate`: 0.00026853060528736673<br>`num_layers`: 2 |
| seq | b | t | `batch_size`: 128<br>`bidirectional`: 1<br>`dropout`: 0.0689489230603657<br>`hidden_size`: 205<br>`learning_rate`: 0.0003650379809438944<br>`num_layers`: 4 |
| seq | m | r | `batch_size`: 64<br>`bidirectional`: 0<br>`dropout`: 0.3018353905795891<br>`hidden_size`: 215<br>`learning_rate`: 0.0003162361873723625<br>`num_layers`: 3 |
| seq | m | rsd | `batch_size`: 64<br>`bidirectional`: 0<br>`dropout`: 0.4003909678178784<br>`hidden_size`: 162<br>`learning_rate`: 0.00015375463691345078<br>`num_layers`: 4 |
| seq | m | t | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.0431854975529545<br>`hidden_size`: 254<br>`learning_rate`: 0.0012591834598857969<br>`num_layers`: 3 |

---

## KNN

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | rsd | `algorithm`: ball_tree<br>`leaf_size`: 2<br>`n_neighbors`: 23<br>`p`: 1<br>`weights`: uniform |
| com | b | t | `algorithm`: kd_tree<br>`leaf_size`: 2<br>`n_neighbors`: 43<br>`p`: 3<br>`weights`: uniform |
| com | m | r | `algorithm`: ball_tree<br>`leaf_size`: 22<br>`n_neighbors`: 14<br>`p`: 1<br>`weights`: distance |
| com | m | rsd | `algorithm`: ball_tree<br>`leaf_size`: 39<br>`n_neighbors`: 7<br>`p`: 2<br>`weights`: uniform |
| com | m | t | `algorithm`: auto<br>`leaf_size`: 60<br>`n_neighbors`: 36<br>`p`: 2<br>`weights`: uniform |
| seq | b | r | `algorithm`: brute<br>`leaf_size`: 17<br>`n_neighbors`: 1<br>`p`: 1<br>`weights`: distance |
| seq | b | rsd | `algorithm`: brute<br>`leaf_size`: 9<br>`n_neighbors`: 7<br>`p`: 1<br>`weights`: distance |
| seq | b | t | `algorithm`: brute<br>`leaf_size`: 7<br>`n_neighbors`: 11<br>`p`: 3<br>`weights`: distance |
| seq | m | r | `algorithm`: auto<br>`leaf_size`: 1<br>`n_neighbors`: 19<br>`p`: 1<br>`weights`: distance |
| seq | m | rsd | `algorithm`: auto<br>`leaf_size`: 37<br>`n_neighbors`: 4<br>`p`: 1<br>`weights`: distance |
| seq | m | t | `algorithm`: auto<br>`leaf_size`: 2<br>`n_neighbors`: 4<br>`p`: 1<br>`weights`: distance |

---

## LIGHTGBM

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `colsample_bytree`: 0.9289672733299068<br>`learning_rate`: 0.09025454444746242<br>`max_depth`: 25<br>`min_child_samples`: 13<br>`n_estimators`: 936<br>`num_leaves`: 105<br>`reg_alpha`: 0.001804894496429<br>`reg_lambda`: 0.0003623517790616<br>`subsample`: 0.7059286856269545 |
| com | b | rsd | `colsample_bytree`: 0.9628169095496016<br>`learning_rate`: 0.047534750445206816<br>`max_depth`: 117<br>`min_child_samples`: 43<br>`n_estimators`: 933<br>`num_leaves`: 56<br>`reg_alpha`: 4.885177367609338<br>`reg_lambda`: 0.0001828246895992<br>`subsample`: 0.6587245214274751 |
| com | b | t | `colsample_bytree`: 0.512911463901825<br>`learning_rate`: 0.0024108511722769088<br>`max_depth`: 2<br>`min_child_samples`: 35<br>`n_estimators`: 307<br>`num_leaves`: 58<br>`reg_alpha`: 0.1462242596214006<br>`reg_lambda`: 0.000369806186491<br>`subsample`: 0.8767998526897003 |
| com | m | r | `colsample_bytree`: 0.9789314801529512<br>`learning_rate`: 0.08030266652243445<br>`max_depth`: 115<br>`min_child_samples`: 11<br>`n_estimators`: 963<br>`num_leaves`: 108<br>`reg_alpha`: 7.589249600442021<br>`reg_lambda`: 0.0382856656380888<br>`subsample`: 0.8353974058382515 |
| com | m | rsd | `colsample_bytree`: 0.9439087294376108<br>`learning_rate`: 0.11173603928441912<br>`max_depth`: 107<br>`min_child_samples`: 51<br>`n_estimators`: 996<br>`num_leaves`: 150<br>`reg_alpha`: 5.414897641418154<br>`reg_lambda`: 0.0004116930769459<br>`subsample`: 0.6889339229315667 |
| com | m | t | `colsample_bytree`: 0.5393317347477286<br>`learning_rate`: 0.0017538575470016037<br>`max_depth`: 8<br>`min_child_samples`: 10<br>`n_estimators`: 526<br>`num_leaves`: 20<br>`reg_alpha`: 0.0956423306908862<br>`reg_lambda`: 0.0552241412592213<br>`subsample`: 0.6461335859169426 |
| seq | b | r | `colsample_bytree`: 0.6205511613657414<br>`learning_rate`: 0.04710364281454966<br>`max_depth`: 20<br>`min_child_samples`: 17<br>`n_estimators`: 870<br>`num_leaves`: 24<br>`reg_alpha`: 0.0003260591129996<br>`reg_lambda`: 0.0001851596303538<br>`subsample`: 0.9888180134169136 |
| seq | b | rsd | `colsample_bytree`: 0.9708800809244358<br>`learning_rate`: 0.039965222416558505<br>`max_depth`: 188<br>`min_child_samples`: 15<br>`n_estimators`: 675<br>`num_leaves`: 57<br>`reg_alpha`: 0.0329347900870916<br>`reg_lambda`: 0.0122797670225763<br>`subsample`: 0.6140243618243135 |
| seq | b | t | `colsample_bytree`: 0.7284662212610772<br>`learning_rate`: 0.15520609640980382<br>`max_depth`: 179<br>`min_child_samples`: 42<br>`n_estimators`: 313<br>`num_leaves`: 61<br>`reg_alpha`: 0.000355681143339<br>`reg_lambda`: 0.0279921144687141<br>`subsample`: 0.6451116554231654 |
| seq | m | r | `colsample_bytree`: 0.6438137106623048<br>`learning_rate`: 0.031772373361988196<br>`max_depth`: 153<br>`min_child_samples`: 7<br>`n_estimators`: 699<br>`num_leaves`: 25<br>`reg_alpha`: 0.0005487842857986<br>`reg_lambda`: 0.1445768456737756<br>`subsample`: 0.8391447460923567 |
| seq | m | rsd | `colsample_bytree`: 0.6066286639910227<br>`learning_rate`: 0.042986868710889976<br>`max_depth`: 54<br>`min_child_samples`: 7<br>`n_estimators`: 779<br>`num_leaves`: 113<br>`reg_alpha`: 3.345279051835599<br>`reg_lambda`: 1.2972804587405748<br>`subsample`: 0.970420907651976 |
| seq | m | t | `colsample_bytree`: 0.556084582692781<br>`learning_rate`: 0.11093042360114566<br>`max_depth`: 238<br>`min_child_samples`: 7<br>`n_estimators`: 708<br>`num_leaves`: 44<br>`reg_alpha`: 0.0003084518214679<br>`reg_lambda`: 0.0004240479038087<br>`subsample`: 0.7593752953126881 |

---

## LOGISTIC-REGRESSION

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `C`: 0.0010716438473141<br>`max_iter`: 210<br>`solver`: lbfgs |
| com | b | rsd | `C`: 4.630433707299038<br>`max_iter`: 104<br>`solver`: lbfgs |
| com | b | t | `C`: 32.15890524965171<br>`max_iter`: 104<br>`solver`: liblinear |
| com | m | r | `C`: 0.7558806972881256<br>`max_iter`: 812<br>`solver`: lbfgs |
| com | m | rsd | `C`: 2.739520106345835<br>`max_iter`: 649<br>`solver`: lbfgs |
| com | m | t | `C`: 0.0010013643617682<br>`max_iter`: 800<br>`solver`: liblinear |
| seq | b | r | `C`: 0.6934410874585542<br>`max_iter`: 321<br>`solver`: liblinear |
| seq | b | rsd | `C`: 0.1807279632501315<br>`max_iter`: 491<br>`solver`: liblinear |
| seq | b | t | `C`: 0.807757477957195<br>`max_iter`: 348<br>`solver`: lbfgs |
| seq | m | r | `C`: 0.0129305972561878<br>`max_iter`: 119<br>`solver`: liblinear |
| seq | m | rsd | `C`: 0.1600933573881855<br>`max_iter`: 568<br>`solver`: liblinear |
| seq | m | t | `C`: 9.63576737271217<br>`max_iter`: 920<br>`solver`: lbfgs |

---

## LSTM

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `batch_size`: 32<br>`bidirectional`: 0<br>`dropout`: 0.246705516298405<br>`hidden_size`: 150<br>`learning_rate`: 0.000377977656929799<br>`num_layers`: 2 |
| com | m | r | `batch_size`: 64<br>`bidirectional`: 0<br>`dropout`: 0.3302719016752671<br>`hidden_size`: 101<br>`learning_rate`: 0.00752996057202493<br>`num_layers`: 1 |
| seq | b | r | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.4360497609363115<br>`hidden_size`: 185<br>`learning_rate`: 0.0003723569790624948<br>`num_layers`: 4 |
| seq | b | rsd | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.3537342387981373<br>`hidden_size`: 148<br>`learning_rate`: 0.0003496763013022542<br>`num_layers`: 5 |
| seq | b | t | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.3863840483354122<br>`hidden_size`: 92<br>`learning_rate`: 0.0012467476048340954<br>`num_layers`: 2 |
| seq | m | r | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.032372831720061<br>`hidden_size`: 150<br>`learning_rate`: 0.0003496523185781235<br>`num_layers`: 5 |
| seq | m | rsd | `batch_size`: 64<br>`bidirectional`: 1<br>`dropout`: 0.3832328204754388<br>`hidden_size`: 149<br>`learning_rate`: 0.0002243830534048714<br>`num_layers`: 4 |
| seq | m | t | `batch_size`: 128<br>`bidirectional`: 1<br>`dropout`: 0.4067758432913229<br>`hidden_size`: 87<br>`learning_rate`: 0.00029445407070361027<br>`num_layers`: 3 |

---

## MLP

### Globally Best Parameters (Identical across all setups)
- `activation`: **relu**

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| seq | b | r | `alpha`: 0.0017300115962006<br>`batch_size`: 64<br>`hidden_layer_sizes`: [81,88,42]<br>`learning_rate_init`: 0.0005326047960169 |
| seq | b | rsd | `alpha`: 9.03652676221e-05<br>`batch_size`: 32<br>`hidden_layer_sizes`: [88,80,80,71,51,86]<br>`learning_rate_init`: 0.0035142696426689 |
| seq | b | t | `alpha`: 0.0004879030285264<br>`batch_size`: 256<br>`hidden_layer_sizes`: [55]<br>`learning_rate_init`: 0.0019636790741827 |
| seq | m | r | `alpha`: 0.0007061182351825<br>`batch_size`: 32<br>`hidden_layer_sizes`: [43,68,64,57]<br>`learning_rate_init`: 0.0003421330317769 |
| seq | m | rsd | `alpha`: 0.0002075001996239<br>`batch_size`: 64<br>`hidden_layer_sizes`: [39,48,80,69]<br>`learning_rate_init`: 0.0003688292958549 |
| seq | m | t | `alpha`: 1.21398980663e-05<br>`batch_size`: 64<br>`hidden_layer_sizes`: [71,58,64,71,34,74]<br>`learning_rate_init`: 0.0001541238756674 |

---

## NN

### Globally Best Parameters (Identical across all setups)
- `solver`: **adam**

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| seq | b | r | `activation`: relu<br>`alpha`: 0.000176780821507<br>`batch_size`: 256<br>`hidden_layer_sizes`: [138,115,92]<br>`learning_rate`: constant<br>`learning_rate_init`: 0.0006249477409553 |
| seq | b | rsd | `activation`: relu<br>`alpha`: 0.0012769190606816<br>`batch_size`: 32<br>`hidden_layer_sizes`: [155,155,155]<br>`learning_rate`: constant<br>`learning_rate_init`: 0.0004100228756599 |
| seq | b | t | `activation`: relu<br>`alpha`: 8.1291375584e-06<br>`batch_size`: 64<br>`hidden_layer_sizes`: [79]<br>`learning_rate`: adaptive<br>`learning_rate_init`: 0.00602680605524 |
| seq | m | r | `activation`: tanh<br>`alpha`: 2.32492362378e-05<br>`batch_size`: 64<br>`hidden_layer_sizes`: [127,127,127,127,127,127,127]<br>`learning_rate`: invscaling<br>`learning_rate_init`: 8.14717040162e-05 |
| seq | m | rsd | `activation`: relu<br>`alpha`: 2.46590675605e-05<br>`batch_size`: 64<br>`hidden_layer_sizes`: [33,33]<br>`learning_rate`: invscaling<br>`learning_rate_init`: 0.0007519094358286 |
| seq | m | t | `activation`: relu<br>`alpha`: 8.0812791404e-06<br>`batch_size`: 256<br>`hidden_layer_sizes`: [176,146,117]<br>`learning_rate`: adaptive<br>`learning_rate_init`: 0.0031014996325271 |

---

## RANDOM-FOREST

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `criterion`: log_loss<br>`max_depth`: 152<br>`max_features`: sqrt<br>`min_samples_leaf`: 5<br>`min_samples_split`: 4<br>`n_estimators`: 675 |
| com | b | rsd | `criterion`: log_loss<br>`max_depth`: 173<br>`max_features`: log2<br>`min_samples_leaf`: 9<br>`min_samples_split`: 6<br>`n_estimators`: 789 |
| com | b | t | `criterion`: gini<br>`max_depth`: 14<br>`max_features`: log2<br>`min_samples_leaf`: 1<br>`min_samples_split`: 5<br>`n_estimators`: 11 |
| com | m | r | `criterion`: log_loss<br>`max_depth`: 29<br>`max_features`: log2<br>`min_samples_leaf`: 1<br>`min_samples_split`: 7<br>`n_estimators`: 49 |
| com | m | rsd | `criterion`: log_loss<br>`max_depth`: 172<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 7<br>`n_estimators`: 75 |
| com | m | t | `criterion`: entropy<br>`max_depth`: 168<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 2<br>`n_estimators`: 481 |
| seq | b | r | `criterion`: log_loss<br>`max_depth`: 128<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 2<br>`n_estimators`: 326 |
| seq | b | rsd | `criterion`: gini<br>`max_depth`: 28<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 8<br>`n_estimators`: 938 |
| seq | b | t | `criterion`: gini<br>`max_depth`: 2<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 2<br>`n_estimators`: 165 |
| seq | m | r | `criterion`: gini<br>`max_depth`: 41<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 8<br>`n_estimators`: 471 |
| seq | m | rsd | `criterion`: gini<br>`max_depth`: 210<br>`max_features`: sqrt<br>`min_samples_leaf`: 1<br>`min_samples_split`: 9<br>`n_estimators`: 272 |
| seq | m | t | `criterion`: entropy<br>`max_depth`: 175<br>`max_features`: log2<br>`min_samples_leaf`: 1<br>`min_samples_split`: 7<br>`n_estimators`: 456 |

---

## RNN

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `batch_size`: 128<br>`bidirectional`: 1<br>`dropout`: 0.0643914920665824<br>`hidden_size`: 90<br>`learning_rate`: 0.0004699385429561206<br>`num_layers`: 1 |
| com | b | rsd | `batch_size`: 128<br>`bidirectional`: 1<br>`dropout`: 0.2354198908468739<br>`hidden_size`: 53<br>`learning_rate`: 0.0031331768536540464<br>`num_layers`: 3 |
| com | m | rsd | `batch_size`: 32<br>`bidirectional`: 0<br>`dropout`: 0.1630900775389878<br>`hidden_size`: 253<br>`learning_rate`: 0.0003377064050565965<br>`num_layers`: 4 |
| com | m | t | `batch_size`: 128<br>`bidirectional`: 0<br>`dropout`: 0.4904246748428845<br>`hidden_size`: 175<br>`learning_rate`: 0.000241788689978814<br>`num_layers`: 3 |
| seq | b | r | `batch_size`: 32<br>`bidirectional`: 0<br>`dropout`: 0.3409001500818948<br>`hidden_size`: 204<br>`learning_rate`: 0.00017564844737757174<br>`num_layers`: 5 |
| seq | b | rsd | `batch_size`: 64<br>`bidirectional`: 0<br>`dropout`: 0.0473198831387756<br>`hidden_size`: 80<br>`learning_rate`: 0.001623697726128788<br>`num_layers`: 3 |
| seq | b | t | `batch_size`: 64<br>`bidirectional`: 1<br>`dropout`: 0.3452959772442188<br>`hidden_size`: 155<br>`learning_rate`: 0.0010141758516202866<br>`num_layers`: 4 |
| seq | m | r | `batch_size`: 32<br>`bidirectional`: 1<br>`dropout`: 0.080916556930462<br>`hidden_size`: 155<br>`learning_rate`: 0.00046057009285664776<br>`num_layers`: 4 |
| seq | m | rsd | `batch_size`: 64<br>`bidirectional`: 0<br>`dropout`: 0.4354960474772817<br>`hidden_size`: 218<br>`learning_rate`: 0.0004633483137056976<br>`num_layers`: 3 |
| seq | m | t | `batch_size`: 128<br>`bidirectional`: 1<br>`dropout`: 0.1505360435524651<br>`hidden_size`: 121<br>`learning_rate`: 0.0002762750184504147<br>`num_layers`: 2 |

---

## SVM

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `C`: 9.6488272880413<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: rbf |
| com | b | rsd | `C`: 5.313541464492284<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: linear |
| com | b | t | `C`: 2.003462917791784<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: poly |
| com | m | r | `C`: 0.5959876243263066<br>`degree`: 3<br>`gamma`: auto<br>`kernel`: rbf |
| com | m | rsd | `C`: 2.495228540706066<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: poly |
| com | m | t | `C`: 18.804439247692887<br>`degree`: 5<br>`gamma`: scale<br>`kernel`: poly |
| seq | b | r | `C`: 0.4381626665743902<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: linear |
| seq | b | rsd | `C`: 4.0117594673898<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: rbf |
| seq | b | t | `C`: 1.192212607995688<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: poly |
| seq | m | r | `C`: 33.140679182948325<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: poly |
| seq | m | rsd | `C`: 48.70882585503515<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: rbf |
| seq | m | t | `C`: 0.6308840254133922<br>`degree`: 3<br>`gamma`: scale<br>`kernel`: rbf |

---

## XGBOOST

### Settings Specific Configurations
| Feat | Task | Split | Hyperparameters |
|---|---|---|---|
| com | b | r | `colsample_bylevel`: 0.6416605001721748<br>`colsample_bytree`: 0.8847805603389478<br>`gamma`: 0.02583043486001736<br>`learning_rate`: 0.27069610731886606<br>`max_delta_step`: 16<br>`max_depth`: 86<br>`max_leaves`: 0<br>`min_child_weight`: 0<br>`n_estimators`: 815<br>`reg_alpha`: 0.4995010869054368<br>`reg_lambda`: 17.289006536877793 |
| com | b | rsd | `colsample_bylevel`: 0.6958582175291396<br>`colsample_bytree`: 0.8836252305916994<br>`gamma`: 0.02011039008019562<br>`learning_rate`: 0.2502493787273656<br>`max_delta_step`: 34<br>`max_depth`: 213<br>`max_leaves`: 0<br>`min_child_weight`: 1<br>`n_estimators`: 965<br>`reg_alpha`: 1.1614581713063643<br>`reg_lambda`: 20.74864266549444 |
| com | b | t | `colsample_bylevel`: 0.688421294841253<br>`colsample_bytree`: 0.6863245145627572<br>`gamma`: 0.6862585748867143<br>`learning_rate`: 0.05533298037081448<br>`max_delta_step`: 52<br>`max_depth`: 247<br>`max_leaves`: 27<br>`min_child_weight`: 1<br>`n_estimators`: 14<br>`reg_alpha`: 1.11958589808488<br>`reg_lambda`: 46.9486835549895 |
| com | m | r | `colsample_bylevel`: 0.8794549209550345<br>`colsample_bytree`: 0.6671614042230756<br>`gamma`: 0.0003905371046789823<br>`learning_rate`: 0.2247574477801452<br>`max_delta_step`: 32<br>`max_depth`: 105<br>`max_leaves`: 0<br>`min_child_weight`: 1<br>`n_estimators`: 669<br>`reg_alpha`: 3.993315443853361<br>`reg_lambda`: 64.21142565129729 |
| com | m | rsd | `colsample_bylevel`: 0.2704339476500359<br>`colsample_bytree`: 0.8804751283569838<br>`gamma`: 0.0017380936473341102<br>`learning_rate`: 0.18128020923151944<br>`max_delta_step`: 93<br>`max_depth`: 195<br>`max_leaves`: 0<br>`min_child_weight`: 0<br>`n_estimators`: 430<br>`reg_alpha`: 5.5109804164182155<br>`reg_lambda`: 22.192248429574256 |
| com | m | t | `colsample_bylevel`: 0.7586283057606511<br>`colsample_bytree`: 0.760083061068122<br>`gamma`: 0.44767246118401016<br>`learning_rate`: 0.1199533965368<br>`max_delta_step`: 0<br>`max_depth`: 63<br>`max_leaves`: 10<br>`min_child_weight`: 0<br>`n_estimators`: 10<br>`reg_alpha`: 3.2140770632166378<br>`reg_lambda`: 13.42978610235883 |
| seq | b | r | `colsample_bylevel`: 0.7774345259009513<br>`colsample_bytree`: 0.6555816367552108<br>`gamma`: 0.05106051191774853<br>`learning_rate`: 0.16321135306332865<br>`max_delta_step`: 70<br>`max_depth`: 209<br>`max_leaves`: 17<br>`min_child_weight`: 0<br>`n_estimators`: 978<br>`reg_alpha`: 0.5369019383039318<br>`reg_lambda`: 3.917379239250855 |
| seq | b | rsd | `colsample_bylevel`: 0.8100236638637782<br>`colsample_bytree`: 0.8264089530767307<br>`gamma`: 0.10600283202773356<br>`learning_rate`: 0.11993305447034268<br>`max_delta_step`: 27<br>`max_depth`: 159<br>`max_leaves`: 26<br>`min_child_weight`: 1<br>`n_estimators`: 225<br>`reg_alpha`: 6.632088056996159<br>`reg_lambda`: 67.60893855495061 |
| seq | b | t | `colsample_bylevel`: 0.7933076682762672<br>`colsample_bytree`: 0.8714136337629087<br>`gamma`: 0.00012056878111240276<br>`learning_rate`: 0.2998301057232197<br>`max_delta_step`: 3<br>`max_depth`: 218<br>`max_leaves`: 0<br>`min_child_weight`: 1<br>`n_estimators`: 841<br>`reg_alpha`: 0.0080749896635938<br>`reg_lambda`: 15.722934160724176 |
| seq | m | r | `colsample_bylevel`: 0.8562021086644346<br>`colsample_bytree`: 0.7847389884147001<br>`gamma`: 0.02964634819871684<br>`learning_rate`: 0.13189947446196965<br>`max_delta_step`: 51<br>`max_depth`: 51<br>`max_leaves`: 0<br>`min_child_weight`: 0<br>`n_estimators`: 872<br>`reg_alpha`: 0.8157233094945306<br>`reg_lambda`: 33.2655319857497 |
| seq | m | rsd | `colsample_bylevel`: 0.5028256866587825<br>`colsample_bytree`: 0.827052300900007<br>`gamma`: 0.01325040117338024<br>`learning_rate`: 0.15107132366563125<br>`max_delta_step`: 5<br>`max_depth`: 233<br>`max_leaves`: 30<br>`min_child_weight`: 0<br>`n_estimators`: 703<br>`reg_alpha`: 0.6465161427205146<br>`reg_lambda`: 5.535089361829814 |
| seq | m | t | `colsample_bylevel`: 0.695374540074625<br>`colsample_bytree`: 0.1043310880471406<br>`gamma`: 0.08855991205068713<br>`learning_rate`: 0.08589288558770658<br>`max_delta_step`: 49<br>`max_depth`: 145<br>`max_leaves`: 7<br>`min_child_weight`: 1<br>`n_estimators`: 729<br>`reg_alpha`: 0.2586873622260688<br>`reg_lambda`: 22.327919328104574 |

---

