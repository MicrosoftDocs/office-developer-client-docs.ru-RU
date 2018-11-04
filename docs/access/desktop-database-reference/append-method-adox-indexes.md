---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a02e74bbbc1b24939784a89965bf0757be0cfe
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949406"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="089f0-102">Метод Append (коллекция Indexes в ADOX)</span><span class="sxs-lookup"><span data-stu-id="089f0-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="089f0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="089f0-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="089f0-104">Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="089f0-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="089f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="089f0-105">Syntax</span></span>

<span data-ttu-id="089f0-106">*Индексы*. Добавление*индекса* \[,*столбцы*\]</span><span class="sxs-lookup"><span data-stu-id="089f0-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="089f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="089f0-107">Parameters</span></span>

|<span data-ttu-id="089f0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="089f0-108">Parameter</span></span>|<span data-ttu-id="089f0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="089f0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="089f0-110">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="089f0-110">*Index*</span></span> |<span data-ttu-id="089f0-111">Объект **индекса** для добавления или имя индекса для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="089f0-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="089f0-112">*Столбцы*</span><span class="sxs-lookup"><span data-stu-id="089f0-112">*Columns*</span></span> |<span data-ttu-id="089f0-113">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="089f0-113">Optional.</span></span> <span data-ttu-id="089f0-114">Значение **типа Variant** , который указывает имена столбцов для индексации.</span><span class="sxs-lookup"><span data-stu-id="089f0-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="089f0-115">Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.</span><span class="sxs-lookup"><span data-stu-id="089f0-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="089f0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="089f0-116">Remarks</span></span>

<span data-ttu-id="089f0-117">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="089f0-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="089f0-118">Если поставщик не поддерживает создание индексов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="089f0-118">An error will occur if the provider does not support creating indexes.</span></span>

