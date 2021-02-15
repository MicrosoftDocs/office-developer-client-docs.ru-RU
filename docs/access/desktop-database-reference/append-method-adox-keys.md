---
title: Метод Append (коллекция Keys в ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297090"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="c3921-102">Метод Append (коллекция Keys в ADOX)</span><span class="sxs-lookup"><span data-stu-id="c3921-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="c3921-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3921-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3921-104">Добавляет новый [объект Key](key-object-adox.md) в коллекцию [Keys.](keys-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c3921-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3921-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3921-105">Syntax</span></span>

<span data-ttu-id="c3921-106">*Ключи .* Ключ \[ приложения,*KeyType,* \] \[  \] \[ Столбец ,*RelatedTable* \] \[ ,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="c3921-106">*Keys*.Append *Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c3921-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3921-107">Parameters</span></span>

|<span data-ttu-id="c3921-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c3921-108">Parameter</span></span>|<span data-ttu-id="c3921-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c3921-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c3921-110">*Раздел*</span><span class="sxs-lookup"><span data-stu-id="c3921-110">*Key*</span></span> |<span data-ttu-id="c3921-111">Объект **Key,** который необходимо к приложению, или имя ключа, который необходимо создать и придать.</span><span class="sxs-lookup"><span data-stu-id="c3921-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="c3921-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="c3921-112">*KeyType*</span></span> |<span data-ttu-id="c3921-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c3921-113">Optional.</span></span> <span data-ttu-id="c3921-114">**Длинное** значение, которое указывает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="c3921-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="c3921-115">Параметр *Key* соответствует свойству [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) объекта **Key.**</span><span class="sxs-lookup"><span data-stu-id="c3921-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="c3921-116">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="c3921-116">*Column*</span></span> |<span data-ttu-id="c3921-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c3921-117">Optional.</span></span> <span data-ttu-id="c3921-118">**Строка,** указывавая имя столбца для индексации.</span><span class="sxs-lookup"><span data-stu-id="c3921-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="c3921-119">Параметр *Columns* соответствует значению свойства [Name](name-property-adox.md) объекта [Column.](column-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c3921-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="c3921-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="c3921-120">*RelatedTable*</span></span> |<span data-ttu-id="c3921-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c3921-121">Optional.</span></span> <span data-ttu-id="c3921-122">**Строка,** заданная для имени связанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="c3921-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="c3921-123">Параметр *RelatedTable* соответствует значению свойства **Name** объекта [Table.](table-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c3921-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="c3921-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="c3921-124">*RelatedColumn*</span></span> |<span data-ttu-id="c3921-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c3921-125">Optional.</span></span> <span data-ttu-id="c3921-126">**Строка,** задав имя связанного столбца для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="c3921-126">A **String** value that specifies the name of the related column for a foreign key.</span></span> <span data-ttu-id="c3921-127">Параметр RelatedColumn соответствует значению свойства **Name** объекта **Column.**</span><span class="sxs-lookup"><span data-stu-id="c3921-127">The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c3921-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="c3921-128">Remarks</span></span>

<span data-ttu-id="c3921-129">Параметр *Columns* может принимать имя столбца или массив имен столбцов.</span><span class="sxs-lookup"><span data-stu-id="c3921-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

