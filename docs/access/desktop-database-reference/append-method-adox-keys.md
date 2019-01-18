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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718905"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="c96dc-102">Метод Append (коллекция Keys в ADOX)</span><span class="sxs-lookup"><span data-stu-id="c96dc-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="c96dc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c96dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c96dc-104">Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="c96dc-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c96dc-105">Syntax</span></span>

<span data-ttu-id="c96dc-106">*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="c96dc-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c96dc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c96dc-107">Parameters</span></span>

|<span data-ttu-id="c96dc-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c96dc-108">Parameter</span></span>|<span data-ttu-id="c96dc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c96dc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c96dc-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="c96dc-110">*Key*</span></span> |<span data-ttu-id="c96dc-111">Объект **ключ** для добавления или имя раздела для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="c96dc-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="c96dc-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="c96dc-112">*KeyType*</span></span> |<span data-ttu-id="c96dc-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c96dc-113">Optional.</span></span> <span data-ttu-id="c96dc-114">**Длинное** значение, задающее тип ключа.</span><span class="sxs-lookup"><span data-stu-id="c96dc-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="c96dc-115">Параметр *ключ* соответствует свойство [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) объекта **ключа** .</span><span class="sxs-lookup"><span data-stu-id="c96dc-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="c96dc-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="c96dc-116">*Column*</span></span> |<span data-ttu-id="c96dc-117">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c96dc-117">Optional.</span></span> <span data-ttu-id="c96dc-118">**Строковое** значение, задающее имя столбца для индексирования.</span><span class="sxs-lookup"><span data-stu-id="c96dc-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="c96dc-119">Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="c96dc-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="c96dc-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="c96dc-120">*RelatedTable*</span></span> |<span data-ttu-id="c96dc-121">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c96dc-121">Optional.</span></span> <span data-ttu-id="c96dc-122">**Строковое** значение, задающее имя связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="c96dc-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="c96dc-123">Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="c96dc-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="c96dc-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="c96dc-124">*RelatedColumn*</span></span> |<span data-ttu-id="c96dc-125">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c96dc-125">Optional.</span></span> <span data-ttu-id="c96dc-126">**Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="c96dc-126">A **String** value that specifies the name of the related column for a foreign key.</span></span> <span data-ttu-id="c96dc-127">Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="c96dc-127">The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c96dc-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="c96dc-128">Remarks</span></span>

<span data-ttu-id="c96dc-129">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="c96dc-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

