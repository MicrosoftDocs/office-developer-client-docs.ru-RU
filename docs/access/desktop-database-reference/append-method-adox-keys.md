---
title: Добавьте метод (ADOX ключей)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ba46c922ff9fc27da0abc1908f6ffaff8e997ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879461"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="491c5-102">Добавьте метод (ADOX ключей)</span><span class="sxs-lookup"><span data-stu-id="491c5-102">Append Method (ADOX Keys)</span></span>


<span data-ttu-id="491c5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="491c5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="491c5-104">Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="491c5-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="491c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="491c5-105">Syntax</span></span>

<span data-ttu-id="491c5-106">*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="491c5-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="491c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="491c5-107">Parameters</span></span>

  - <span data-ttu-id="491c5-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="491c5-108">*Key*</span></span>

  - <span data-ttu-id="491c5-109">Объект **ключ** для добавления или имя раздела для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="491c5-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="491c5-110">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="491c5-110">*KeyType*</span></span>

  - <span data-ttu-id="491c5-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="491c5-111">Optional.</span></span> <span data-ttu-id="491c5-112">**Длинное** значение, задающее тип ключа.</span><span class="sxs-lookup"><span data-stu-id="491c5-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="491c5-113">Параметр *ключ* соответствует свойство [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) объекта **ключа** .</span><span class="sxs-lookup"><span data-stu-id="491c5-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="491c5-114">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="491c5-114">*Column*</span></span>

  - <span data-ttu-id="491c5-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="491c5-115">Optional.</span></span> <span data-ttu-id="491c5-116">**Строковое** значение, задающее имя столбца для индексирования.</span><span class="sxs-lookup"><span data-stu-id="491c5-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="491c5-117">Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="491c5-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="491c5-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="491c5-118">*RelatedTable*</span></span>

  - <span data-ttu-id="491c5-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="491c5-119">Optional.</span></span> <span data-ttu-id="491c5-120">**Строковое** значение, задающее имя связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="491c5-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="491c5-121">Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="491c5-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="491c5-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="491c5-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="491c5-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="491c5-123">Optional.</span></span> <span data-ttu-id="491c5-124">**Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="491c5-124">A **String** value that specifies the name of the related column for a foreign key.</span></span> <span data-ttu-id="491c5-125">Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="491c5-125">The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="491c5-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="491c5-126">Remarks</span></span>

<span data-ttu-id="491c5-127">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="491c5-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

