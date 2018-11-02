---
title: Метод Append (коллекция Indexes в ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41eb1cc67dd5a2058f9c5673db381f0bc9067454
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921483"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="971b2-102">Метод Append (коллекция Indexes в ADOX)</span><span class="sxs-lookup"><span data-stu-id="971b2-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="971b2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="971b2-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="971b2-104">Добавляет новый объект [индекса](index-object-adox.md) в коллекцию [индексов](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="971b2-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="971b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="971b2-105">Syntax</span></span>

<span data-ttu-id="971b2-106">*Индексы*. Добавление*индекса* \[,*столбцы*\]</span><span class="sxs-lookup"><span data-stu-id="971b2-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="971b2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="971b2-107">Parameters</span></span>

  - <span data-ttu-id="971b2-108">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="971b2-108">*Index*</span></span>

  - <span data-ttu-id="971b2-109">Объект **индекса** для добавления или имя индекса для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="971b2-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="971b2-110">*Столбцы*</span><span class="sxs-lookup"><span data-stu-id="971b2-110">*Columns*</span></span>

  - <span data-ttu-id="971b2-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="971b2-111">Optional.</span></span> <span data-ttu-id="971b2-112">Значение **типа Variant** , который указывает имена столбцов для индексации.</span><span class="sxs-lookup"><span data-stu-id="971b2-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="971b2-113">Параметр *столбцы* соответствует значения свойства [Name](name-property-adox.md) [столбца](column-object-adox.md) объект или объекты.</span><span class="sxs-lookup"><span data-stu-id="971b2-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="971b2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="971b2-114">Remarks</span></span>

<span data-ttu-id="971b2-115">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="971b2-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="971b2-116">Если поставщик не поддерживает создание индексов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="971b2-116">An error will occur if the provider does not support creating indexes.</span></span>

