---
title: Метод Append (коллекция Columns в ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711233"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="c3493-102">Метод Append (коллекция Columns в ADOX)</span><span class="sxs-lookup"><span data-stu-id="c3493-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="c3493-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3493-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3493-104">Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="c3493-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3493-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3493-105">Syntax</span></span>

<span data-ttu-id="c3493-106">*Столбцы*.</span><span class="sxs-lookup"><span data-stu-id="c3493-106">*Columns*.</span></span> <span data-ttu-id="c3493-107">Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="c3493-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c3493-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="c3493-108">Parameters</span></span>

|<span data-ttu-id="c3493-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="c3493-109">Parameter</span></span>|<span data-ttu-id="c3493-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c3493-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c3493-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="c3493-111">*Column*</span></span> |<span data-ttu-id="c3493-112">Объект для добавления **столбца** или имя столбца для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="c3493-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="c3493-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="c3493-113">*Type*</span></span> |<span data-ttu-id="c3493-114">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c3493-114">Optional.</span></span> <span data-ttu-id="c3493-115">Значение типа **Long** , определяющее тип данных столбца.</span><span class="sxs-lookup"><span data-stu-id="c3493-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="c3493-116">Параметр *типа* соответствует свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="c3493-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="c3493-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="c3493-117">*DefinedSize*</span></span> |<span data-ttu-id="c3493-118">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c3493-118">Optional.</span></span> <span data-ttu-id="c3493-119">Значение типа **Long** , определяет размер столбца.</span><span class="sxs-lookup"><span data-stu-id="c3493-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="c3493-120">Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="c3493-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="c3493-121">После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c3493-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


