---
title: 'Chapter 2: Getting Data'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d3df907e1dbe220caab58541b7c3eba605ef2f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481746"
---
# <a name="chapter-2-getting-data"></a>Chapter 2: Getting Data


**Применимо к**: Access 2013 | Office 2013

Предыдущей главе представлены четыре основных операций, используемых при создании приложения ADO: получение данных, анализ данных, изменение данных и обновление данных. В этой главе нацеливаются на сведения о концепциях, имеющих отношение к первой операции: получение данных.

Несколько объектов ADO можно играют роль в этой операции. Сначала подключиться к источнику данных с помощью объекта ADO- **подключение** (что иногда будут создаваться неявно). Затем передайте инструкции к источнику данных о требуется сделать с помощью объекта ADO **команды** (который также может быть создан неявно). В результате передачи команды к источнику данных и получения ответа обычно будут представлены в объект ADO **Recordset** .

Для получения данных, приложения должны быть в связи с источником данных, например СУБД, хранилище файлов или файлов с разделителями-запятыми. Эти подключения представляет *подключение* — среды, необходимые для обмена данными.

Объектная модель ADO представляет концепцию соединение с объект **подключения** — foundation, на какие ADO построения функциональные возможности. Объект **подключения** предназначен для:

  - Определите сведения, необходимые ADO для взаимодействия с источниками данных и создание сеансов.

  - Определение возможности транзакций сеанса.

  - Дают возможность создания и выполнения команд в источнике данных.

  - Представлены сведения о разработке источника данных в виде строк схемы. Дополнительные сведения о наборах строк схемы [OpenSchema](openschema-method-ado.md)см.
