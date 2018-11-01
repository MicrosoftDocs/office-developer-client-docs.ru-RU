---
title: Index.Clustered Property (DAO)
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
ms.openlocfilehash: 2748be69677cacee246864303d2ff57dad9235b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875590"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, представляет ли объект **индекса** кластеризованных индекса для таблицы (только для рабочих областей Microsoft Access). Для чтения и записи, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Кластерные

*выражение* Выражение, возвращающее объект **индекса** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это тип данных Boolean, который имеет **значение True** , если объект **индекса** представляет кластеризованных индекса.

Некоторые форматы базы данных рабочего стола IISAM используйте кластеризованных индексов. Кластерные индекса состоит из одного или нескольких неключевые поля, которые, взятые вместе, упорядочить все записи в таблице в предопределенном порядке. Кластерные индекса предоставляет эффективного доступа к записям в таблице, в котором значения индекса могут быть уникальным.

Свойство **Clustered** — чтение и запись для нового объекта **индекс** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **индексов** .


> [!NOTE]
> <UL>
> <LI>
> <P>Базами данных, ядро базы данных Microsoft Access игнорировать свойство <STRONG>Clustered</STRONG> ядро базы данных Microsoft Access поддерживает кластеризованных индексов.</P>
> <LI>
> <P>Для источников данных ODBC <STRONG>Clustered</STRONG> свойство всегда возвращает <STRONG>значение False</STRONG>; не удается обнаружить ли источник данных ODBC имеет кластеризованных индекса.</P></LI></UL>


