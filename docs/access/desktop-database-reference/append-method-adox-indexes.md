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
# <a name="append-method-adox-indexes"></a><span data-ttu-id="d42a3-102">Метод Append (коллекция Indexes в ADOX)</span><span class="sxs-lookup"><span data-stu-id="d42a3-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="d42a3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d42a3-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="d42a3-104">Добавляет новый [объект Index](index-object-adox.md) в коллекцию [Indexes.](indexes-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="d42a3-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d42a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d42a3-105">Syntax</span></span>

<span data-ttu-id="d42a3-106">*Индексы*. Индекс *приложения* \[ ,*столбцы*\]</span><span class="sxs-lookup"><span data-stu-id="d42a3-106">*Indexes*.Append *Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d42a3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d42a3-107">Parameters</span></span>

|<span data-ttu-id="d42a3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d42a3-108">Parameter</span></span>|<span data-ttu-id="d42a3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d42a3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d42a3-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d42a3-110">*Index*</span></span> |<span data-ttu-id="d42a3-111">Объект **Index** для приложения или имя индекса для создания и приложения.</span><span class="sxs-lookup"><span data-stu-id="d42a3-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="d42a3-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="d42a3-112">*Columns*</span></span> |<span data-ttu-id="d42a3-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d42a3-113">Optional.</span></span> <span data-ttu-id="d42a3-114">Значение **Variant,** которое указывает имя (ы) индексировать столбец(ы).</span><span class="sxs-lookup"><span data-stu-id="d42a3-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="d42a3-115">Параметр *Columns* соответствует значению (s) свойства [Name](name-property-adox.md) объекта или объектов [Column.](column-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="d42a3-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d42a3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d42a3-116">Remarks</span></span>

<span data-ttu-id="d42a3-117">Параметр *Columns* может принимать имя столбца или массив имен столбцов.</span><span class="sxs-lookup"><span data-stu-id="d42a3-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="d42a3-118">Ошибка возникает, если поставщик не поддерживает создание индексов.</span><span class="sxs-lookup"><span data-stu-id="d42a3-118">An error will occur if the provider does not support creating indexes.</span></span>

