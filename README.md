# Diplom_SkillFactory

В данном проекте предлагается решить задачу по классифиции текста от информационной группы SCAN "Интерфакс". 

SCAN (https://scan-interfax.ru/) - это система Международной информационной группы "Интерфакс", предназначенная для комплексного решения задач в сфере управления репутацией и анализа эффективности PR. Решает задачи по мониторингу СМИ и соцсетей, анализу медиа-поля, проверке деловой репутации компаний и персон, позволяет пользователям оперативно реагировать на появление негатива в СМИ и соцмедиа, путём осуществления автоматизированного сбора и анализа публичной информации из более чем 60 тысяч источников.

Одной из функциональных возможностей SCAN является фактографический анализ новостной информации - выделение контекстов, в которых упоминается событие или действие некоторого субъекта на заданную тематику и с заданной тональностью.
На текущий момент SCAN умеет определять контексты более чем по 800 различным темам. Разработка каждой темы представляет собой длительный процесс по предварительному сбору и анализу большого корпуса текстовой информации для выделения характерных фраз, с последующим написанием машинных правил на специальном DSL (domain-specific language), в котором задействован целый отдел прикладных лингвистов.

В данном проекте предлагается принять участие в решении значимой для проекта SCAN задачи, которая позволяет расширить спектр выделяемых системой контекстов и снизит нагрузку на лингвистов:

Разработать модель автоматизированного поиска контекстов на заданные тематики. В данном случае важна семантическая близость к уже проработанным контекстам, чтобы не требовалось описывать каждый контекст в рамках одной тематики машинными правилами на специальном DSL:

В качестве искомого контекста может выступать как часть предложения исходного текста, так и целое предложение, или даже набор предложений на ту же тему.

  Предоставленные данные состоят из наборов размеченных корпусов по 50 различным тематикикам и искомого контекста. В качестве искомого контекста может выступать как часть предложения исходного текста, так и целое предложение, или даже набор предложений на ту же тему. 
  В процессе работы над проектом, был произведен детальный анализ текста, а также применены методы по визуализации. 
  При построении модели были использованы методы от scikit-learn:
  - Logistic Regression
  - LinearSVC
  - Методы зибыточной выборки (RandomOverSampler, SMOTE)
  Метод поиска оптимальных параметров GridSearchCV
  Ансамблевые методы классификации (StackingClassifier)
  Также попробовал применить transformers от  Huggingface ("cointegrated/rubert-tiny", "DeepPavlov/rubert-base-cased-sentence", )
