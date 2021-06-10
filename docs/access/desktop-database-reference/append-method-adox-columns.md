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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297125"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="f5689-102">Метод Append (коллекция Columns в ADOX)</span><span class="sxs-lookup"><span data-stu-id="f5689-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="f5689-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5689-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5689-104">Добавляет новый [объект Column](column-object-adox.md) в коллекцию [Столбцы.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f5689-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5689-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5689-105">Syntax</span></span>

<span data-ttu-id="f5689-106">*Столбцы*.</span><span class="sxs-lookup"><span data-stu-id="f5689-106">*Columns*.</span></span> <span data-ttu-id="f5689-107">Столбец *приложения* \[ ,*Тип* \] \[ ,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="f5689-107">Append *Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="f5689-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5689-108">Parameters</span></span>

|<span data-ttu-id="f5689-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="f5689-109">Parameter</span></span>|<span data-ttu-id="f5689-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f5689-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f5689-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="f5689-111">*Column*</span></span> |<span data-ttu-id="f5689-112">Объект **Column** для приложения или имя столбца для создания и приложения.</span><span class="sxs-lookup"><span data-stu-id="f5689-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="f5689-113">*Тип*</span><span class="sxs-lookup"><span data-stu-id="f5689-113">*Type*</span></span> |<span data-ttu-id="f5689-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f5689-114">Optional.</span></span> <span data-ttu-id="f5689-115">**Длинное** значение, которое указывает тип данных столбца.</span><span class="sxs-lookup"><span data-stu-id="f5689-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="f5689-116">Параметр *Type* соответствует свойству [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) объекта **Column.**</span><span class="sxs-lookup"><span data-stu-id="f5689-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="f5689-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="f5689-117">*DefinedSize*</span></span> |<span data-ttu-id="f5689-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f5689-118">Optional.</span></span> <span data-ttu-id="f5689-119">**Длинное** значение, которое указывает размер столбца.</span><span class="sxs-lookup"><span data-stu-id="f5689-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="f5689-120">Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **Column.**</span><span class="sxs-lookup"><span data-stu-id="f5689-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="f5689-121">Ошибка возникает при приложении  столбца к коллекции **Столбцы** индекса, если столбец не существует в таблице, которая уже примыкает к коллекции [Таблицы.](tables-collection-adox.md) [](index-object-adox.md)  [](table-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f5689-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


