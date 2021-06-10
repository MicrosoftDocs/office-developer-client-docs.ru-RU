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
# <a name="indexclustered-property-dao"></a><span data-ttu-id="9bdf3-102">Свойство Index.Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bdf3-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="9bdf3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bdf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bdf3-104">Задает или возвращает значение, которое указывает, представляет ли объект **Index** кластерный индекс для таблицы (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9bdf3-104">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9bdf3-105">Для чтения и записи, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-105">Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bdf3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bdf3-106">Syntax</span></span>

<span data-ttu-id="9bdf3-107">*выражения* . Кластеризация</span><span class="sxs-lookup"><span data-stu-id="9bdf3-107">*expression* .Clustered</span></span>

<span data-ttu-id="9bdf3-108">*выражение* Выражение, возвращаемая **объекту Index.**</span><span class="sxs-lookup"><span data-stu-id="9bdf3-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bdf3-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9bdf3-109">Remarks</span></span>

<span data-ttu-id="9bdf3-110">Параметр или возвращаемая величина — это тип данных Boolean, который является **True,** если объект **Index** представляет кластерный индекс.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="9bdf3-111">В некоторых форматах настольных баз данных IISAM используются кластерные индексы.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-111">Some IISAM desktop database formats use clustered indexes.</span></span> <span data-ttu-id="9bdf3-112">Кластерный индекс состоит из одного или нескольких нестандартных полей, которые, взятые вместе, упорядочение всех записей в таблице в заранее.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-112">A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order.</span></span> <span data-ttu-id="9bdf3-113">Кластерный индекс обеспечивает эффективный доступ к записям в таблице, в которой значения индекса могут быть не уникальными.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-113">A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="9bdf3-114">Свойство **Clustered** — это свойство чтения и записи для нового объекта **Index,** еще не пристроенного к коллекции и только для чтения существующего объекта **Index** в коллекции **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="9bdf3-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="9bdf3-115">Базы данных баз данных Microsoft Access игнорируют свойство **Clustered,** так как двигатель базы данных Microsoft Access не поддерживает кластерные индексы.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="9bdf3-116">Для источников данных ODBC свойство **Clustered** всегда возвращает **false;** он не определяет, имеет ли источник данных ODBC кластерный индекс.</span><span class="sxs-lookup"><span data-stu-id="9bdf3-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


