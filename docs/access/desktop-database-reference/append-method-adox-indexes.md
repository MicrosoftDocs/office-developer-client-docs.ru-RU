---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297097"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="ebb41-102">Метод Append (коллекция Indexes в ADOX)</span><span class="sxs-lookup"><span data-stu-id="ebb41-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="ebb41-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebb41-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ebb41-104">Добавляет новый объект [index](index-object-adox.md) в коллекцию [indexes](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb41-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebb41-105">Syntax</span></span>

<span data-ttu-id="ebb41-106">*Индексы*. Добавление*индекса* \[,*столбцов*\]</span><span class="sxs-lookup"><span data-stu-id="ebb41-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="ebb41-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebb41-107">Parameters</span></span>

|<span data-ttu-id="ebb41-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="ebb41-108">Parameter</span></span>|<span data-ttu-id="ebb41-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ebb41-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ebb41-110">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="ebb41-110">*Index*</span></span> |<span data-ttu-id="ebb41-111">Объект **index** , который требуется добавить, или имя индекса, который требуется создать и добавить.</span><span class="sxs-lookup"><span data-stu-id="ebb41-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="ebb41-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="ebb41-112">*Columns*</span></span> |<span data-ttu-id="ebb41-113">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="ebb41-113">Optional.</span></span> <span data-ttu-id="ebb41-114">Значение **типа Variant** , задающее имена столбцов для индексирования.</span><span class="sxs-lookup"><span data-stu-id="ebb41-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="ebb41-115">Параметр *Columns* соответствует значениям свойства [Name](name-property-adox.md) объекта [Column](column-object-adox.md) или объектов.</span><span class="sxs-lookup"><span data-stu-id="ebb41-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ebb41-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebb41-116">Remarks</span></span>

<span data-ttu-id="ebb41-117">Параметр *Columns* может принимать либо имя столбца, либо массив имен столбцов.</span><span class="sxs-lookup"><span data-stu-id="ebb41-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="ebb41-118">Если поставщик не поддерживает создание индексов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="ebb41-118">An error will occur if the provider does not support creating indexes.</span></span>

