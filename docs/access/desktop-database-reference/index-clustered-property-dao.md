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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706708"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="00642-102">Свойство Index.Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="00642-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="00642-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00642-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00642-104">Задает или возвращает значение, указывающее, представляет ли объект **индекса** кластеризованных индекса для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="00642-104">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="00642-105">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="00642-105">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="00642-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00642-106">Syntax</span></span>

<span data-ttu-id="00642-107">*выражение* . Кластерные</span><span class="sxs-lookup"><span data-stu-id="00642-107">*expression* .Clustered</span></span>

<span data-ttu-id="00642-108">*выражение* Выражение, возвращающее объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="00642-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="00642-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="00642-109">Remarks</span></span>

<span data-ttu-id="00642-110">Параметр или возвращаемое значение — это тип данных Boolean, который имеет **значение True** , если объект **индекса** представляет кластеризованных индекса.</span><span class="sxs-lookup"><span data-stu-id="00642-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="00642-111">Некоторые форматы базы данных рабочего стола IISAM используйте кластеризованных индексов.</span><span class="sxs-lookup"><span data-stu-id="00642-111">Some IISAM desktop database formats use clustered indexes.</span></span> <span data-ttu-id="00642-112">Кластерные индекса состоит из одного или нескольких неключевые поля, которые, взятые вместе, упорядочить все записи в таблице в предопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="00642-112">A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order.</span></span> <span data-ttu-id="00642-113">Кластерные индекса предоставляет эффективного доступа к записям в таблице, в котором значения индекса могут быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="00642-113">A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="00642-114">Свойство **Clustered** — чтение и запись для нового объекта **индекс** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **индексов** .</span><span class="sxs-lookup"><span data-stu-id="00642-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="00642-115">Базами данных, ядро базы данных Microsoft Access игнорировать свойство **Clustered** ядро базы данных Microsoft Access поддерживает кластеризованных индексов.</span><span class="sxs-lookup"><span data-stu-id="00642-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="00642-116">Для источников данных ODBC **Clustered** свойство всегда возвращает **значение False**; не удается обнаружить ли источник данных ODBC имеет кластеризованных индекса.</span><span class="sxs-lookup"><span data-stu-id="00642-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


