==============================================================
XLM-EMO: Multilingual Emotion Prediction in Social Media Text
==============================================================


.. image:: https://img.shields.io/pypi/v/xlm_emo.svg
        :target: https://pypi.python.org/pypi/xlm_emo

.. image:: https://img.shields.io/travis/MilaNLProc/xlm_emo.svg
        :target: https://travis-ci.com/MilaNLProc/xlm_emo


Abstract
--------

Detecting emotion in text allows social and computational scientists to study how people behave and react to online events. However, developing these tools for different languages requires data that is not always available. This paper collects the available emotion detection datasets across 19 languages. We train a multilingual emotion prediction model for social media data, XLM-EMO. The model shows competitive performance in a zero-shot setting, suggesting it is helpful in the context of low-resource languages. We release our model to the community so that interested researchers can directly use it.

See the papers for additional details:

Bianchi, F., Nozza, & D., Hovy. "XLM-EMO: Multilingual Emotion Prediction in Social Media Text". In Proceedings of the 12th Workshop on Computational Approaches to Subjectivity, Sentiment and Social Media Analysis (Forthcoming). Association for Computational Linguistics, 2022. <https://milanlproc.github.io/publication/2022-xlmemo-multilingual-emotion-prediction>

----------

* Free software: MIT license

Installing
----------

.. code-block:: bash

    pip install -U xlm-emo

**Important**: If you want to use CUDA you need to install the correct version of
the CUDA systems that matches your distribution, see `PyTorch <https://pytorch.org/get-started/locally/>`__.

Features
--------

.. code-block:: python

    from xlm_emo.classifier import  EmotionClassifier
    ec = EmotionClassifier()

    ec.predict(["senti testa di cazzo", "I am very happy"])

    >> ["anger", "joy"]


Models
------

+-----------+---------------------------------------------+----------------------+
| Model     | Link                                        | Macro F1 on Test Set |
+-----------+---------------------------------------------+----------------------+
| XLM-EMO-T | https://huggingface.co/MilaNLProc/xlm-emo-t | 0.85                 |
+-----------+---------------------------------------------+----------------------+
| XLM-EMO-B | TBD                                         | TBD                  |
+-----------+---------------------------------------------+----------------------+
| XLM-EMO-L | TBD                                         | TBD                  |
+-----------+---------------------------------------------+----------------------+

Reference
---------

If you use this tool please cite the following paper:

.. code-block::

    @inproceedings{bianchi-etal-2022-xlmemo,
    title = {{XLM-EMO}: Multilingual Emotion Prediction in Social Media Text},
    author = "Bianchi, Federico and Nozza, Debora and Hovy, Dirk",
    booktitle = "Proceedings of the 12th Workshop on Computational Approaches to Subjectivity, Sentiment and Social Media Analysis",
    year = "2022",
    publisher = "Association for Computational Linguistics"
    }

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
