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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707558"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="320fb-102">Метод Append (коллекция Indexes в ADOX)</span><span class="sxs-lookup"><span data-stu-id="320fb-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="320fb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="320fb-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="320fb-104">Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="320fb-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="320fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="320fb-105">Syntax</span></span>

<span data-ttu-id="320fb-106">*Индексы*. Добавление*индекса* \[,*столбцы*\]</span><span class="sxs-lookup"><span data-stu-id="320fb-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="320fb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="320fb-107">Parameters</span></span>

|<span data-ttu-id="320fb-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="320fb-108">Parameter</span></span>|<span data-ttu-id="320fb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="320fb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="320fb-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="320fb-110">*Index*</span></span> |<span data-ttu-id="320fb-111">Объект **индекса** для добавления или имя индекса для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="320fb-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="320fb-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="320fb-112">*Columns*</span></span> |<span data-ttu-id="320fb-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="320fb-113">Optional.</span></span> <span data-ttu-id="320fb-114">Значение **типа Variant** , который указывает имена столбцов для индексации.</span><span class="sxs-lookup"><span data-stu-id="320fb-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="320fb-115">Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.</span><span class="sxs-lookup"><span data-stu-id="320fb-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="320fb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="320fb-116">Remarks</span></span>

<span data-ttu-id="320fb-117">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="320fb-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="320fb-118">Если поставщик не поддерживает создание индексов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="320fb-118">An error will occur if the provider does not support creating indexes.</span></span>

