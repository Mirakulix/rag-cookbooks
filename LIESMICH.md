[![LinkedIn](https://img.shields.io/badge/LinkedIn-follow-blue)](https://www.linkedin.com/company/athina-ai/posts/?feedView=all)&nbsp;
[![Twitter](https://img.shields.io/twitter/follow/AthinaAI?label=Follow%20@AthinaAI&style=social)](https://x.com/AthinaAI)&nbsp;
[![Share](https://img.shields.io/badge/share-000000?logo=x&logoColor=white)](https://x.com/intent/tweet?text=Check%20out%20this%20project%20on%20GitHub:%20https://github.com/athina-ai/rag-cookbooks)&nbsp;
[![Share](https://img.shields.io/badge/share-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/sharing/share-offsite/?url=https://github.com/athina-ai/rag-cookbooks)&nbsp;
[![Share](https://img.shields.io/badge/share-FF4500?logo=reddit&logoColor=white)](https://www.reddit.com/submit?title=Check%20out%20this%20project%20on%20GitHub:%20https://github.com/athina-ai/rag-cookbooks)

>Wenn Sie dieses Repository hilfreich finden, würden wir uns über einen Stern⭐️ freuen

# Fortgeschrittene + Agentische RAG Cookbooks👨🏻‍💻
Willkommen zu dieser umfassenden Sammlung fortgeschrittener und agentischer Retrieval-Augmented Generation (RAG) Techniken.

## Einführung🚀
RAG ist eine beliebte Methode, die Genauigkeit und Relevanz verbessert, indem sie die richtigen Informationen aus zuverlässigen Quellen findet und in nützliche Antworten umwandelt. Dieses Repository behandelt die effektivsten fortgeschrittenen und agentischen RAG-Techniken mit klaren Implementierungen und Erklärungen.

Das Hauptziel dieses Repositories ist es, eine hilfreiche Ressource für Forscher und Entwickler bereitzustellen, die fortgeschrittene RAG-Techniken in ihren Projekten einsetzen möchten. Die Entwicklung dieser Techniken von Grund auf ist zeitaufwändig, und geeignete Evaluierungsmethoden zu finden kann herausfordernd sein. Dieses Repository vereinfacht den Prozess durch sofort einsetzbare Implementierungen und Anleitungen zur Evaluierung.

>[!NOTE]
>Dieses Repository beginnt mit einfachem RAG als Grundlage und schreitet zu fortgeschrittenen und agentischen Techniken fort. Es enthält auch Forschungspapiere/Referenzen für jede RAG-Technik zur weiteren Vertiefung.

## Einführung in RAG💡
Große Sprachmodelle werden auf einem festen Datensatz trainiert, was ihre Fähigkeit einschränkt, private oder aktuelle Informationen zu verarbeiten. Sie können manchmal "halluzinieren" und dabei falsche, aber glaubwürdig klingende Antworten liefern. Fine-Tuning kann helfen, ist aber teuer und nicht ideal für wiederholtes Training mit neuen Daten. Das RAG-Framework löst dieses Problem, indem es externe Dokumente nutzt, um die Antworten des LLM durch kontextbezogenes Lernen zu verbessern. RAG stellt sicher, dass die vom LLM bereitgestellten Informationen nicht nur kontextuell relevant, sondern auch präzise und aktuell sind.

![final diagram](https://github.com/user-attachments/assets/508b3a87-ac46-4bf7-b849-145c5465a6c0)

RAG besteht aus vier Hauptkomponenten:

**Indexierung:** Zunächst werden Dokumente (in beliebigem Format) in Chunks aufgeteilt und Embeddings für diese Chunks erstellt. Diese Embeddings werden dann einem Vektorspeicher hinzugefügt.

**Retriever:** Dann findet der Retriever die relevantesten Dokumente basierend auf der Benutzeranfrage, unter Verwendung von Techniken wie Vektorähnlichkeit aus dem Vektorspeicher.

**Augment:** Danach kombiniert der Augment-Teil die Benutzeranfrage mit dem abgerufenen Kontext zu einem Prompt und stellt sicher, dass das LLM die notwendigen Informationen für akkurate Antworten hat.

**Generate:** Schließlich werden die kombinierte Anfrage und der Prompt an das Modell übergeben, das dann die endgültige Antwort auf die Benutzeranfrage generiert.

Diese Komponenten von RAG ermöglichen es dem Modell, auf aktuelle, genaue Informationen zuzugreifen und Antworten basierend auf externem Wissen zu generieren. Um jedoch sicherzustellen, dass RAG-Systeme effektiv funktionieren, ist es wichtig, ihre Leistung zu evaluieren.

## RAG Evaluierung📊
Die Evaluierung von RAG-Anwendungen ist wichtig, um zu verstehen, wie gut diese Systeme funktionieren. Wir können sehen, wie effektiv sie Informationsabruf mit generativen Modellen kombinieren, indem wir ihre Genauigkeit und Relevanz überprüfen. Diese Evaluierung hilft, RAG-Anwendungen in Aufgaben wie Textzusammenfassung, Chatbots und Frage-Antwort-Systemen zu verbessern. Sie identifiziert auch Verbesserungsbereiche und stellt sicher, dass diese Systeme vertrauenswürdige Antworten liefern, während sich Informationen ändern. Insgesamt hilft effektive Evaluierung, die Leistung zu optimieren und Vertrauen in RAG-Anwendungen für den praktischen Einsatz aufzubauen. Diese Notebooks enthalten eine End-to-End RAG-Implementierung + RAG-Evaluierung in Athina AI.

![evals diagram](https://github.com/user-attachments/assets/65c2b5af-a931-40c5-b006-87567aef019f)

## Fortgeschrittene RAG-Techniken⚙️
Hier sind die Details aller fortgeschrittenen RAG-Techniken, die in diesem Repository behandelt werden.

| Technik                    | Tools                        | Beschreibung                                                       | Notebooks |
|---------------------------------|------------------------------|--------------------------------------------------------------|-----------|
| Naive RAG      | LangChain, Pinecone, Athina AI                    | Kombiniert abgerufene Daten mit LLMs für einfache und effektive Antworten.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/naive_rag.ipynb) |
| Hybrid RAG      | LangChain, Chromadb, Athina AI                    | Kombiniert Vektorsuche und traditionelle Methoden wie BM25 für besseren Informationsabruf.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/hybrid_rag.ipynb) |
| Hyde RAG      | LangChain, Weaviate, Athina AI                    | Erstellt hypothetische Dokument-Embeddings, um relevante Informationen für eine Anfrage zu finden.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/hyde_rag.ipynb) |
| Parent Document Retriever      | LangChain, Chromadb, Athina AI                    | Teilt große Dokumente in kleine Teile und ruft das vollständige Dokument ab, wenn ein Teil zur Anfrage passt.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/parent_document_retriever.ipynb) |
| RAG fusion      | LangChain, LangSmith, Qdrant, Athina AI                    | Generiert Unter-Anfragen, bewertet Dokumente mit Reciprocal Rank Fusion und verwendet Top-Ergebnisse für genaue Antworten.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/fusion_rag.ipynb) |
| Contextual RAG      | LangChain, Chromadb, Athina AI                    | Komprimiert abgerufene Dokumente, um nur relevante Details für präzise und genaue Antworten zu behalten.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/contextual_rag.ipynb) |
| Rewrite Retrieve Read     | LangChain, Chromadb, Athina AI                    | Verbessert die Anfrage, ruft bessere Daten ab und generiert genaue Antworten.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/rewrite_retrieve_read.ipynb) |
| Unstructured RAG     | LangChain, LangGraph, FAISS, Athina AI, Unstructured                    | Diese Methode ist für die Verarbeitung von Dokumenten konzipiert, die Text, Tabellen und Bilder kombinieren.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/advanced_rag_techniques/basic_unstructured_rag.ipynb) |

## Agentische RAG-Techniken⚙️
Hier sind die Details aller agentischen RAG-Techniken, die in diesem Repository behandelt werden.

| Technik                    | Tools                        | Beschreibung                                                       | Notebooks |
|---------------------------------|------------------------------|--------------------------------------------------------------|-----------|
| Basic Agentic RAG      | LangChain, FAISS, Athina AI                    | Agentisches RAG verwendet KI-Agenten, um Antworten mit Tools wie Vektordb und Websuchen zu finden und zu generieren.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/agentic_rag_techniques/basic_agentic_rag.ipynb) |
| Corrective RAG      | LangChain, LangGraph, Chromadb, Athina AI                    | Verfeinert relevante Dokumente, entfernt irrelevante oder führt die Websuche durch.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/agentic_rag_techniques/corrective_rag.ipynb) |
| Self RAG     | LangChain, LangGraph, FAISS, Athina AI                    | Reflektiert über abgerufene Daten, um genaue und vollständige Antworten sicherzustellen.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/agentic_rag_techniques/self_rag.ipynb) |
| Adaptive RAG      | LangChain, LangGraph, FAISS, Athina AI                    | Passt Abrufmethoden basierend auf Anfragetyp an, verwendet indexierte Daten oder Websuche.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/agentic_rag_techniques/adaptive_rag.ipynb) |
| ReAct RAG      | LangChain, LangGraph, FAISS, Athina AI                    | System, das Reasoning und Retrieval für kontextbewusste Antworten kombiniert.| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/athina-ai/rag-cookbooks/blob/main/agentic_rag_techniques/react_rag.ipynb) |

## Demo🎬
Eine kurze Demo, wie jedes Notebook funktioniert:

https://github.com/user-attachments/assets/c6f17961-40a1-4cca-ab1f-2c8fa3d71a7a

## Erste Schritte🛠️
Klonen Sie zunächst dieses Repository mit folgendem Befehl:
```bash
git clone https://github.com/athina-ai/rag-cookbooks.git
```
Navigieren Sie dann zum Projektverzeichnis:
```bash
cd rag-cookbooks
```
Sobald Sie sich im 'rag-cookbooks' Verzeichnis befinden, folgen Sie der detaillierten Implementierung für jede Technik.

## Entwickler + Mitwirkende👨🏻‍💻
[![Contributors](https://contrib.rocks/image?repo=athina-ai/cookbooks)](https://github.com/athina-ai/cookbooks/graphs/contributors)

## Mitwirken🤝
Wenn Sie eine neue Technik oder Verbesserung vorschlagen möchten, freuen wir uns über Beiträge aus der Community!

## Lizenz📝
Dieses Projekt steht unter der [MIT Lizenz](LICENSE)