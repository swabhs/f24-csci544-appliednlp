---
title: Detailed Calendar
nav_exclude: false
include_nav_home: true
toc: true
---

# Detailed Calendar

Required and additional readings, to be updated (bi)weekly. Additional readings are not mandatory.



<table>
  <thead>
  <tr>
    <th width="5%">Week</th>
    <th width="5%">Date</th>
    <th width="30%">Class Topics</th>
    <th width="40%">Readings</th>
    <th width="13%">Work Due</th>
  </tr>
  </thead>
  <tbody>
  {% for week in site.data.calendar %}
    {% for day in week.days %}
      <tr>
        {% if forloop.index == 1 %}
        <td rowspan="{{week.size}}">{{week.week}}</td>
        {% endif %}
        <td>{{day.date}}</td>
        <!-- <td>{{day.theme}}</td> -->
        <td class="cal-content">
        {% if day.slides %}
          <a href="{{day.slides}}">{{day. theme}}</a>
        {% else %}
          {{day.theme}}
        {% endif %}
        </td>
        <td class="cal-content">
          {% if day.readingslink %}
            <a href="{{day.readingslink}}">{{day.readings}}</a>
          {% else if day.readings %}
            {{day.readings}}
          {% endif %}
          {% if day.additional %}
            {% if day.additionallink %}
              <a href="{{day.additionallink}}"><b>Additional:</b> {{day.additional}}</a>
            {% else %}
              <b>Additional:</b> {{day.additional}}
            {% endif %}
          {% endif %}
        </td>
        <td class="cal-content">{{day.due}}</td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>

<!-- ## Introduction to Language Models

### **Jan 08**{: .label .label-purple } &nbsp; Lecture 1 Introduction  &nbsp; <span class="fs-3"> [Slides](./){: .btn .btn-red} </span>
No Required Readings


### **Jan 10**{: .label .label-purple } &nbsp; Lecture 2: n-gram LMs I  &nbsp; <span class="fs-3"> [Slides](./){: .btn .btn-red} </span>
#### Required Readings
  - Jurafsky and Martin, [Chap 3.1-3.3](https://web.stanford.edu/~jurafsky/slp3/3.pdf)

### **Jan 17**{: .label .label-purple } &nbsp; Lecture 3: n-gram LMs II   &nbsp; <span class="fs-3"> [Slides](./){: .btn .btn-red} </span>
#### Required Readings
- Jurafsky and Martin, [Chap 3.4-3.7](https://web.stanford.edu/~jurafsky/slp3/3.pdf)

#### Additional Readings
- Mitchell, [Chap 2, Estimating Probabilities](https://www.cs.cmu.edu/~tom/mlbook/Joint_MLE_MAP.pdf) -->





<!--


## Early Neural Language Models
### [Lecture 4](https://drive.google.com/file/d/15uKD511ocHUeQ4FlXWrttpRCTyv3hoUO/view?usp=sharing):  Word Embeddings   &nbsp;**Aug 30**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 6.1-6.7](https://web.stanford.edu/~jurafsky/slp3/6.pdf)

### [Lecture 5](https://drive.google.com/file/d/1xN5FiqtutlFrhID64qDGA3DqaZMIZfMh/view?usp=sharing):  Word Embeddings II  &nbsp; **Sep 6**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 6.8-6.12](https://web.stanford.edu/~jurafsky/slp3/6.pdf)

#### Additional Readings
- [Mikolov et al., ICLR 2013](https://arxiv.org/abs/1301.3781). Efficient Estimation of Word Representations in Vector Space
- [Mikolov et al., NeurIPS 2013](https://arxiv.org/abs/1310.4546) Distributed Representations of Words and Phrases and their Compositionality
- [Jay Al Ammar. Illustrated Word2Vec](https://jalammar.github.io/illustrated-word2vec/)
<!-- - [Collobert et al., 2011](https://arxiv.org/abs/1103.0398)

### [Lecture 6](https://drive.google.com/file/d/1VqPJrY0hL0Mq4Pn_r87UKIz6V2UxmSgh/view?usp=drive_link):  Logistic Regression I &nbsp; **Sep 11**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 5](https://web.stanford.edu/~jurafsky/slp3/5.pdf)

### [Lecture 7](https://drive.google.com/file/d/1PKGOQs5jPOEexAy2hhGyR3Q8H6u09Gf3/view?usp=drive_link):  Logistic Regression II &nbsp; **Sep 13**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 5](https://web.stanford.edu/~jurafsky/slp3/5.pdf)


### [Lecture 8](https://drive.google.com/file/d/19e5hdBGAhiSC6lysiz_KuoDrsvUIzKID/view?usp=sharing):  Feedforward Neural Network Language Models  &nbsp; **Sep 18**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 7](https://web.stanford.edu/~jurafsky/slp3/7.pdf)



### [Lecture 9](https://drive.google.com/file/d/1zDcs-xUC84r__y55llHolcZsXisB1PEX/view?usp=drive_link):  Recurrent Neural Network Language Models  &nbsp; **Sep 20**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 9.1-9.2](https://web.stanford.edu/~jurafsky/slp3/9.pdf)





## Modern Neural Language Models

### [Lecture 10](https://drive.google.com/file/d/1Yxj2W5Rhj_oHCI_arn4S9VJLFR8sv1V7/view?usp=sharing): Sequence-to-Sequence and Attention  &nbsp; **Sep 25**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 9.3.2-9.3.3; 9.7-9.8](https://web.stanford.edu/~jurafsky/slp3/9.pdf)



### [Lecture 11](https://drive.google.com/file/d/1lJaaQmkqXD_La_dpueox7ilU0mT3LYqc/view?usp=drive_link):  Transformers Building Blocks  &nbsp; **Sep 27**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 10.1](https://web.stanford.edu/~jurafsky/slp3/10.pdf)

### [Lecture 12](https://docs.google.com/presentation/d/1ElK3Ldhk0Co7R-_Y2CBkjDIFiOtz6dvyAehr-jrO7R0/edit?usp=sharing):  Invited Lecture - Language Grounding by Jesse Thomason &nbsp; **Oct 2**{: .label .label-green }


### [Lecture 13](https://colab.research.google.com/drive/1HpNvYzMFMK2IHLnBOGGWCQKw5qScRGxn?usp=sharing):  PyTorch for Transformers  &nbsp; **Oct 4**{: .label .label-green }
#### Additional Readings
- Iyyer CS685 Spring 2023 [Tokenization](https://people.cs.umass.edu/~miyyer/cs685/slides/tokenization.pdf)


### [Lecture 14](https://drive.google.com/file/d/1Dfcc4VAvlRMS6KUxnmeRsohiqU2pPiAB/view?usp=drive_link):  Transformer Building Blocks II  &nbsp; **Oct 16**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 10.2](https://web.stanford.edu/~jurafsky/slp3/10.pdf)

## Large Language Models


### [Lecture 15](https://drive.google.com/file/d/1KMQm7CdJKD_DKIqVWTOg-ZYYmkDM9cpM/view?usp=drive_link):  Pre-training Transformers  &nbsp; **Oct 18**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 11.1-11.2](https://web.stanford.edu/~jurafsky/slp3/11.pdf)


### [Lecture 16](https://drive.google.com/file/d/1Gpf0Bf-oNI340XCRH0ZJ9pF30KYR6hjP/view?usp=sharing): Pretraining Transformers II  &nbsp; **Oct 23**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 11.3](https://web.stanford.edu/~jurafsky/slp3/11.pdf)


### [Lecture 17](https://drive.google.com/file/d/1nZ2mZxR41ZySuzL76DCWSbox3c2tExyg/view?usp=sharing): Generating from Language Models  &nbsp; **Oct 25**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 10.4](https://web.stanford.edu/~jurafsky/slp3/11.pdf)


### [Lecture 18](https://drive.google.com/file/d/1jbYAOMpSFzhMm37iGlBWlbrwenYfeYiO/view?usp=sharing): Generating from Language Models II  &nbsp; **Oct 30**{: .label .label-green }
#### Required Readings
- Jurafsky and Martin, [Chap 13.5.2](https://web.stanford.edu/~jurafsky/slp3/13.pdf)
#### Additional Readings
- [Holtzmann et al., 2020](https://arxiv.org/abs/1904.09751)
- [WordPiece Modeling](https://huggingface.co/learn/nlp-course/chapter6/6?fw=pt)


### [Lecture 19](https://drive.google.com/file/d/1hlnkr0eZsh1fRMTU-DexWTh3yxVF4nrn/view?usp=sharing): Generating from Language Models II  &nbsp; **Nov 1**{: .label .label-green }
#### Additional Readings
- [Zhao et al., 2021](https://arxiv.org/abs/2102.09690)
- [Wei et al., 2022](https://arxiv.org/abs/2201.11903)


### [Lecture 20](https://drive.google.com/file/d/1U8Ha-6tmsQKosryLnULhvRFOg3NnIad4/view?usp=sharing): LLMs: Limitations and Harms  &nbsp; **Nov 6**{: .label .label-green }
#### Additional Readings
- [McGuffie and Newhouse, 2020](https://arxiv.org/abs/2009.06807)
- [Bender et al., 2021](https://dl.acm.org/doi/10.1145/3442188.3445922)
- [Dziri et al., 2022](https://aclanthology.org/2022.naacl-main.387/)


### [Lecture 21](https://drive.google.com/file/d/1UVj9YS-YFDJ8b0vJMdDvi5BJPJvK-MC6/view?usp=sharing): RLHF &nbsp; **Nov 8**{: .label .label-green }
#### Additional Readings
- [Chip Huyen’s blog post on RLHF](https://huyenchip.com/2023/05/02/rlhf.html): Great balance of humor and technical details with many references for detailed information.
- [HuggingFace Blog Post](https://huggingface.co/blog/rlhf): Illustrating RLHF by Nathan Lambert et al.: mainly focuses on the RLHF algorithm itself, providing a brief history of RL and sharing seminal work that led to RLHF and practical tools for using RLHF.
- [Argilla Blog Post](https://argilla.io/blog/mantisnlp-rlhf-part-1/): Finetuning an LLM: RLHF and alternatives
- [Yoav Goldberg’s post](https://gist.github.com/yoavg/6bff0fecd65950898eba1bb321cfbd81): Hypotheses on why RLHF works.
- [Proximal Policy Optimization (PPO): The Key to LLM Alignment](https://cameronrwolfe.substack.com/p/proximal-policy-optimization-ppo): more detail on the PPO algorithm and how it improves on previous RL algorithms. -->




