# Ausarbeitung vom Paper "Machine Learning Meets Databases" von Stephan Günnemann

Link: https://www.dropbox.com/s/iomhkm5von8kg5e/Machine%20Learning%20Meets%20Databases.pdf?dl=0

## A Brief Introduction to Machine Learning

### Types of Learning

#### Supervised Learning

#### Unsupervised Learning

#### Semi-supervised learning

#### Reinforcement learning

### Machine Learning Models and Algorithms

- The result generated by a Machine Learning (ML) algorithm is usually called a model, which indeed can often be thought of as a function which maps an input to an output.
- ML usually involves two phases:
  - In the training (or learning) phase a model is learned based on previously observed data.
  - In the application (or prediction) phase the learned model is applied to new data.
- Ability to correctly process new data instances that differ from those seen during training is known as generalization (main goal of ML) -> optimal for complex data.
- Sof Machine Learning in the last years stems from the
  availability of (i) massive amounts of (labeled) training data
  which allows to comprehensively learn the target domain,
  and (ii) extensive compute power which allows to train models
  based on these data. In particular the use of Graphics
  Processing Units (GPUs) has reduced the time for training
  complex models significantly.

## Machine Learning and Its Relation to Other Data-Driven Sciences

### Knowledge Discovery and Data Mining

### Database Systems

#### Machine Learning in Database Systems

#### Machine Learning for Database Systems

## Data Management Systems Offering Machine Learning Functionality

### Requirements of Machine Learning

#### Scalable Training

#### Flexible Consistency

#### Support for Models/Parameters

#### Ease of Use I – Language Support

#### Ease of Use II – Abstraction

### Machine Learning in Relational DBMSs

- Die meisten Systeme führen Machine Learning-Algorithmen entweder über user-defined fu (UDF) aus, oder die SQL-Sprache wird um Machine Learning / Data Analytics-Funktionen erweitert.

- Ausführung von UDFs aber Systeme könne sie nicht optimieren.

- Main-memory relational database Hyper bietet noch 2 weitere Wege an:

  - Es schlägt eine Erweiterung von SQL über einen Iterationsoperator vor.

  - Es implementiert analytische Operatoren im Datenbankkern, die durch neuartige SQL-Lambda-Ausdrücke direkt in der SQL-Abfrage flexibel gesteuert werden können.

- Oracle Data Miner integriert das Konzept von ML models. Über spezielle Funktionen werden Trainingsdaten verwendet, um Modelle zu erstellen. Später können diese Modelle verwendet werden, um Daten mit SQL zu testen. Die Ergebnisse der Algorithmen werden in relationalen Tabellen gespeichert.

- Weitere Erweiterungen relationaler DBMS sind LogicBlox und SimSQL

### Machine Learning in Distributed Big Data Systems

- Die Notwendigkeit, extrem große Daten zu speichern und zu verarbeiten, hat zum Aufkommen von verteilten Big-Data-Systemen wie Hadoop MapReduce, Spark und Flink geführt.

- Schon früh libs für MapReduce gebaut aber wegen fehlende Funktion von In-Memory-Operationen und Caching hat zu sehr langsamen Algorithmen geführt.

- Bei Spark und Flink besser weil dort spezielle iterative In-Memory-Fähigkeiten besitzen, haben sie besseren ML support.

  - Sowohl Spark als auch Flink bieten eine Vielzahl von vorinstallierten Machine-Learning-Algorithmen über Bibliotheken (MLlib, FlinkML), wodurch das Skalierungspotenzial des Systems genutzt werden kann.

## Discussion

- ML schon länger in KDD vorhanden aber in DBMS noch tnicht entwickelt. Macht aber Sinn wenn Trainingsdaten dynamisch sind oder Datenstruktur zu Beginn unklar ist.

- Fragwürdig ob beide Themengebiete fusioniert werden sollten, da das Training von komplexen ML Models sehr viel Zeit kosten könnten. Nichtsdestotrotz schon erarbeitete Models könnten einen riesen Voteil in DBMS sein.