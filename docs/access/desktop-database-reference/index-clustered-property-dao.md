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
ms.openlocfilehash: 4e7bd39d3329c83ec2a26fbef11e3a3b4e51e760
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921307"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="deab0-102">Свойство Index.Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="deab0-102">Index.Clustered property (DAO)</span></span>


<span data-ttu-id="deab0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="deab0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="deab0-104">Задает или возвращает значение, указывающее, представляет ли объект **индекса** кластеризованных индекса для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="deab0-104">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="deab0-105">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="deab0-105">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="deab0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deab0-106">Syntax</span></span>

<span data-ttu-id="deab0-107">*выражение* . Кластерные</span><span class="sxs-lookup"><span data-stu-id="deab0-107">*expression* .Clustered</span></span>

<span data-ttu-id="deab0-108">*выражение* Выражение, возвращающее объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="deab0-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="deab0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="deab0-109">Remarks</span></span>

<span data-ttu-id="deab0-110">Параметр или возвращаемое значение — это тип данных Boolean, который имеет **значение True** , если объект **индекса** представляет кластеризованных индекса.</span><span class="sxs-lookup"><span data-stu-id="deab0-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="deab0-111">Некоторые форматы базы данных рабочего стола IISAM используйте кластеризованных индексов.</span><span class="sxs-lookup"><span data-stu-id="deab0-111">Some IISAM desktop database formats use clustered indexes.</span></span> <span data-ttu-id="deab0-112">Кластерные индекса состоит из одного или нескольких неключевые поля, которые, взятые вместе, упорядочить все записи в таблице в предопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="deab0-112">A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order.</span></span> <span data-ttu-id="deab0-113">Кластерные индекса предоставляет эффективного доступа к записям в таблице, в котором значения индекса могут быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="deab0-113">A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="deab0-114">Свойство **Clustered** — чтение и запись для нового объекта **индекс** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **индексов** .</span><span class="sxs-lookup"><span data-stu-id="deab0-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="deab0-115">Базами данных, ядро базы данных Microsoft Access игнорировать свойство <STRONG>Clustered</STRONG> ядро базы данных Microsoft Access поддерживает кластеризованных индексов.</span><span class="sxs-lookup"><span data-stu-id="deab0-115">Microsoft Access database engine databases ignore the <STRONG>Clustered</STRONG> property because the Microsoft Access database engine doesn't support clustered indexes.</span></span></P>
> <LI>
> <P><span data-ttu-id="deab0-116">Для источников данных ODBC <STRONG>Clustered</STRONG> свойство всегда возвращает <STRONG>значение False</STRONG>; не удается обнаружить ли источник данных ODBC имеет кластеризованных индекса.</span><span class="sxs-lookup"><span data-stu-id="deab0-116">For ODBC data sources the <STRONG>Clustered</STRONG> property always returns <STRONG>False</STRONG>; it does not detect whether or not the ODBC data source has a clustered index.</span></span></P></LI></UL>


