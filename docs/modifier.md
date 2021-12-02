# 修饰参数用例

## 语义修饰参数

### ARGM-COM（伴随 Comitatives）

⾏使动作的伴随者：与谁⼀起完成了某项动作。

=== "例句一"
    I sang a song with my sister.

    | ARG0 | REL  | ARG1   | *ARGM-COM*           |
    | :--: | :--: | :----: | :------------------: |
    | I    | sang | a song | ***with my sister*** |

### ARGM-LOC（方位 Locatives）

动作的发⽣地点；可为物理⽅位，也可为抽象位置。

=== "例句一"
    He was born in Japan.

    | ARG1 | REL  | *ARGM-LOC*     |
    | :--: | :--: | :------------: |
    | He   | born | ***in Japan*** |

=== "例句二"
    In his ruling, Judge Curry added an additional $55 million to the commission ’s calculations.

    | *ARGM-LOC*          | ARG0        | REL   | ARG1                       | ARG2                              |
    | :-----------------: | :---------: | :---: | :------------------------: | :-------------------------------: |
    | ***In his ruling*** | Judge Curry | added | an additional $ 55 million | to the commission ’s calculations |

### ARGM-DIR（方向 Directional）

动作的发⽣路径；当没有明确路径时，应标注为 LOC。例如，walk along the road 属⽅向，walk around the countryside 属⽅位。

=== "例句一"
    The congressman snapped back that there had been enough studies of the issue.

    | ARG0            | REL     | *ARGM-DIR* | ARG1                                            |
    | :-------------: | :-----: | :--------: | :---------------------------------------------: |
    | The congressman | snapped | ***back*** | that there had been enough studies of the issue |

### ARGM-GOL（目标 Goal）

动作的⽬标、对象等，或实际动作的终点，⼀般以 for 和 to 为标志词。

=== "例句一"
    The child fed the cat for her mother.

    | ARG0      | REL | ARG1    | *ARGM-GOL*           |
    | :-------: | :-: | :-----: | :------------------: |
    | The child | fed | the cat | ***for her mother*** |

=== "例句二"
    We publicized to the masses our determination to fight against evil.

    | ARG0 | REL        | *ARGM-GOL*          | ARG1                                    |
    | :--: | :--------: | :-----------------: | :-------------------------------------: |
    | We   | publicized | ***to the masses*** | our determination to fight against evil |

### ARGM-MNR（形式 Manner）

动作是“怎样”⾏使的，可⽤以 how 开头的问句对其提问。

=== "例句一"
    Workers mechanically mixed the dry fibers in a process used to make filters.

    | ARG0    | *ARGM-MNR*         | REL   | ARG1           | ARGM-LOC                          |
    | :-----: | :----------------: | :---: | :------------: | :-------------------------------: |
    | Workers | ***mechanically*** | mixed | the dry fibers | in a process used to make filters |

### ARGM-TMP（时间 Temporal）

动作与时间相关的信息，例如：

- 发⽣时间：in 1987、last Wednesday、soon、immediately
- 发生频率：often、always、sometimes
- 发生顺序：first、ninth、last（注意与空间顺序区分）
- 重复：again、repeatedly

=== "例句一"
    Four of the five surviving workers have asbestos-related diseases, including three with recently diagnosed cancer.

    | *ARGM-TMP*     | REL       | ARG2   |
    | :------------: | :-------: | :----: |
    | ***recently*** | diagnosed | cancer |

### ARGM-EXT（程度 Extent）

动作导致的数量变化，主要包括：

- 数值：“They raised prices **by 15 percent**.”
- 量词：a lot、least、incredibly、extremely、really
- ⽐较词：“He raised prices **more than she did**.”

=== "例句一"
    "An active 55-year-old in Boca Raton may care more about Senior Olympic games," she says.

    | ARG0                                 | ARGM-MOD | REL  | *ARGM-EXT* | ARG1                       |
    | :----------------------------------: | :------: | :--: | :--------: | :------------------------: |
    | An active 55- year-old in Boca Raton | may      | care | ***more*** | about Senior Olympic games |

### ARGM-REC（反身代词 Reciprocals）

作副词时的 himself、itself、themselves、each other、own 等，通常指⽰句中的 ARG1 成分。

=== "例句一"
    But voters decided that if the stadium was such a good idea someone would build it himself.

    | ARGM-ADV                            | ARG0    | ARGM-MOD | REL   | ARG1 | *ARGM-REC*    |
    | :---------------------------------: | :-----: | :------: | :---: | :--: | :-----------: |
    | if the stadium was such a good idea | someone | would    | build | it   | ***himself*** |

### ARGM-PRD（次要述谓 Secondary Prediction）

⾃⾝具备谓词结构的修饰语，⼀般修饰动词的其他参数⽽⾮动词本⾝。典型例⼦包括：

- 结果体：“The boys pinched them **dead**.”“She kicked the locker lid **shut**.”
- 描述体：“**Rosy-cheeked**, Santa came down the chimney.”
- as 短语：“It is supplied **as security in the transaction**.”（注意与“as ... as ...”结构区分）

=== "例句一"
    This wage inflation is bleeding the NFL dry, the owners contend.

    | ARG0                | REL      | ARG1    | *ARGM-PRD* |
    | :-----------------: | :------: | :-----: | :--------: |
    | This wage inflation | bleeding | the NFL | ***dry***  |

### ARGM-PRP（动机从句 Purpose）

动作的动机，典型标志有 for、to、in order to 和 so that 等。

=== "例句一"
    More than a few CEOs say the redcarpet treatment tempts them to return to a heartland city for future meetings.

    | ARG1 | REL    | ARG4                | *ARGM-PRP*                |
    | :--: | :----: | :-----------------: | :-----------------------: |
    | them | return | to a heartland city | ***for future meetings*** |

### ARGM-CAU（原因从句 Cause）

动作的理由，典型标志有 because、due to 以及 why 引导的从句。若标注者⽆法分别参数的属性是动机还是原因，默认选择原因作为标签。

=== "例句一"
    Pro-forma balance sheets clearly show why Cray Research favored the spinoff.

    | *ARGM-CAU* | ARG0          | REL     | ARG1        |
    | :--------: | :-----------: | :-----: | :---------: |
    | ***why***  | Cray Research | favored | the spinoff |

## 语法修饰参数

### ARGM-MOD（情态动词 Modal）

包括 will、may、can、must、shall、might、should、could 和 would 等。例句略。

### ARGM-NEG（否定词 Negation）

包含 not、n't、never、no longer 以及其他表否定的句⼦。注意 **never** 默认标记为 NEG ⽽⾮ TMP。例句略。

### ARGM-DIS（连接词 Discourse）

句间其连系作⽤的词或词组，如 also、however、too、as well、but、and、as we've seen before、instead、on the other hand、for instance 等。注意，连接词须产⽣句间的连系作⽤，⽤在句⼦内部的连词仅能归为 ARGM-ADV。

=== "例句一"
    But for now , they ’re looking forward to their winter meeting – Boca in February.

    | *ARGM-DIS* | ARGM-TMP | ARG0 | REL             | ARG1                                       |
    | :--------: | :------: | :--: | :-------------: | :----------------------------------------: |
    | ***But***  | for now  | they | looking forward | to their winter meeting – Boca in February |

=== "例句二"
    The notification also clarifies the requirements of the evaluation.

    | ARG0             | *ARGM-DIS* | REL       | ARG1                               |
    | :--------------: | :--------: | :-------: | :--------------------------------: |
    | The notification | ***also*** | clarifies | the requirements of the evaluation |

## 通用修饰参数

### ARGM-ADV（副词 Adverbials）

修饰事件、但不属于以上分类的状语成分。与 MNR 不同，MNR 修饰动作本⾝，⽽ ADV 修饰整个句⼦。主要类型包括：

- 时间：“Treasures are just lying around, **waiting to be picked up**.”
- 内涵：probably、possibly
- 焦点：only、even
- 句子作者的评价、态度、观点、⾏为：fortunately、really、legally、frankly speaking
- 由 given that、despite、except for、if 等关键词引导的从句

=== "例句一"
    Happily, she sang.（表示“I am happy that she sang”。注意与表示 “She sang happily.” 的情况区分，这里 happily 标注为 ARGM-MNR）

    | *ARGM-ADV*    | ARG0 | REL  |
    | :-----------: | :--: | :--: |
    | ***Happily*** | she  | sang |

### ARGM-ADJ（形容词 Adjectival）

与副词类似，但适⽤于名词谓词的修饰（即定语）；请不要在修饰动词谓词或形容词谓词时使⽤该标签。

=== "例句一"
    Investors have witnessed a drastic distortion in the market.

    | *ARGM-ADJ*    | REL        | ARGM-LOC      |
    | :-----------: | :--------: | :-----------: |
    | ***drastic*** | distortion | in the market |

## 特殊结构参数

### ARGM-LVB（轻动词 Light Verb）

当伸展动词（即轻动词与名词的组合）中的名词作谓词时，使⽤该标签标注与之匹配的轻动词。注意在轻动词作谓词时，应当为谓词选择轻动词⾓⾊集，⽽不是使⽤该标签。

=== "例句一"
    The public criticized that the government has made a cowardly decision to please international corporations.

    | ARG0       | *ARGM-LVB* | ARGM-ADJ | REL      | ARG1                                 |
    | :--------: | :--------: | :------: | :------: | :----------------------------------: |
    | government | ***made*** | cowardly | decision | to please international corporations |

### ARGM-CXN（结构词 Construction）

仅针对形容词谓词使⽤。当形容词谓词是某个固定搭配的⼀部分，且该固定搭配存在不匹配上述任何⼀个标签的成分时，应将它们统⼀标注为单⼀搭配成分。可能的搭配包括：

- ⽐较：“Their price is **more** expensive **than the average**.”“She came **about as** soon **as possible**.”
- 程度：“It is **too** late **to recover**.”“We are tough **enough to beat everybody**.”
- 同步递进：“**The better the system is**, **the more** complicated it should be.”

=== "例句一"
    The workers are not united enough to give powerful reactions against the new policy.

    | ARG0        | ARGM-NEG | REL    | *ARGM-CXN*                                                     |
    | :---------: | :------: | :-----:| :------------------------------------------------------------: |
    | the workers | not      | united | ***enough to give powerful reactions against the new policy*** |
