---
title: Свойство Index.Clustered (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291854"
---
# <a name="indexclustered-property-dao"></a>Свойство Index.Clustered (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, представляет ли объект **Index** кластерный индекс для таблицы (только для рабочей области Microsoft Access). Для чтения и записи, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение .* Кластерная

*выражение* Выражение, которое возвращает объект **Index.**

## <a name="remarks"></a>Заметки

Значение параметра или возвращаемого значения — это тип данных Boolean, значение **True,** если объект **Index** представляет кластерный индекс.

В некоторых форматах баз данных IISAM используются кластерные индексы. Кластерный индекс состоит из одного или нескольких нестандартных полей, которые в совокупности упорядочают все записи в таблице в предварительно заранее задаваемом порядке. Кластерный индекс обеспечивает эффективный доступ к записям в таблице, в которой значения индекса могут быть не уникальными.

Свойство **Clustered** доступно для чтения и записи для нового объекта **Index,** еще не примеся к коллекции и доступного только для чтения для существующего объекта **Index** в коллекции **Indexes.**

> [!NOTE]
> - Базы данных ядер баз данных Microsoft Access игнорируют свойство **Clustered,** так как ядер баз данных Microsoft Access не поддерживает кластерные индексы.
> - Для источников данных ODBC свойство **Clustered** всегда возвращает **false;** Он не определяет, имеет ли источник данных ODBC кластерный индекс.


