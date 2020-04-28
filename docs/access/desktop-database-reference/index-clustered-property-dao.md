---
title: Свойство index. Clustered (DAO)
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
# <a name="indexclustered-property-dao"></a><span data-ttu-id="8dfd9-102">Свойство index. Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="8dfd9-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="8dfd9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dfd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8dfd9-104">Задает или возвращает значение, которое указывает, представляет ли объект **index** кластеризованный индекс для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8dfd9-104">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8dfd9-105">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-105">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfd9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dfd9-106">Syntax</span></span>

<span data-ttu-id="8dfd9-107">*Expression* . Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="8dfd9-107">*expression* .Clustered</span></span>

<span data-ttu-id="8dfd9-108">*Expression (выражение* ) Выражение, возвращающее объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="8dfd9-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfd9-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8dfd9-109">Remarks</span></span>

<span data-ttu-id="8dfd9-110">Параметр или возвращаемое значение — это логический тип данных, который имеет значение **true** , если объект **index** представляет кластеризованный индекс.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="8dfd9-111">В некоторых форматах баз данных IISAM для рабочих станций используются кластеризованные индексы.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-111">Some IISAM desktop database formats use clustered indexes.</span></span> <span data-ttu-id="8dfd9-112">Кластеризованный индекс состоит из одного или нескольких неключевых полей, которые, взятые вместе, упорядочивают все записи в таблице в предварительно заданном порядке.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-112">A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order.</span></span> <span data-ttu-id="8dfd9-113">Кластеризованный индекс обеспечивает эффективный доступ к записям в таблице, в которой значения индекса не могут быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-113">A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="8dfd9-114">Свойство **Clustered** доступно для чтения и записи для нового объекта **index** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **index** в коллекции **indexes** .</span><span class="sxs-lookup"><span data-stu-id="8dfd9-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="8dfd9-115">Базы данных ядра СУБД Microsoft Access игнорируют свойство **Clustered** , так как ядро СУБД Microsoft Access не поддерживает кластеризованные индексы.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="8dfd9-116">Для источников данных ODBC свойство **Clustered** всегда возвращает **значение false**; Он не определяет, имеется ли кластеризованный индекс в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="8dfd9-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


