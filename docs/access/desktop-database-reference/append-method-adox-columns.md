---
title: Метод Append (коллекция Columns в ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 12e79802587874aacb5b47a56387e331b8148069
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026374"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="08e50-102">Метод Append (коллекция Columns в ADOX)</span><span class="sxs-lookup"><span data-stu-id="08e50-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="08e50-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08e50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08e50-104">Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="08e50-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08e50-105">Syntax</span></span>

<span data-ttu-id="08e50-106">*Столбцы*.</span><span class="sxs-lookup"><span data-stu-id="08e50-106">*Columns*.</span></span> <span data-ttu-id="08e50-107">Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="08e50-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="08e50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08e50-108">Parameters</span></span>

|<span data-ttu-id="08e50-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="08e50-109">Parameter</span></span>|<span data-ttu-id="08e50-110">Описание</span><span class="sxs-lookup"><span data-stu-id="08e50-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="08e50-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="08e50-111">*Column*</span></span> |<span data-ttu-id="08e50-112">Объект для добавления **столбца** или имя столбца для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="08e50-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="08e50-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="08e50-113">*Type*</span></span> |<span data-ttu-id="08e50-114">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="08e50-114">Optional.</span></span> <span data-ttu-id="08e50-115">Значение типа **Long** , определяющее тип данных столбца.</span><span class="sxs-lookup"><span data-stu-id="08e50-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="08e50-116">Параметр *типа* соответствует свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="08e50-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="08e50-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="08e50-117">*DefinedSize*</span></span> |<span data-ttu-id="08e50-118">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="08e50-118">Optional.</span></span> <span data-ttu-id="08e50-119">Значение типа **Long** , определяет размер столбца.</span><span class="sxs-lookup"><span data-stu-id="08e50-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="08e50-120">Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="08e50-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="08e50-121">После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="08e50-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


