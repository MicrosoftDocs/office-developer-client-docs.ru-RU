---
title: Метод Append (коллекция Keys в ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cc1d03fe68093959406a444419128b161f3b5be4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921477"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="0fb57-102">Метод Append (коллекция Keys в ADOX)</span><span class="sxs-lookup"><span data-stu-id="0fb57-102">Append method (ADOX Keys)</span></span>


<span data-ttu-id="0fb57-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fb57-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0fb57-104">Добавляет новый объект [ключа](key-object-adox.md) в коллекцию [ключей](keys-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb57-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb57-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fb57-105">Syntax</span></span>

<span data-ttu-id="0fb57-106">*Ключи*. Добавьте*ключ* \[,*KeyType* \] \[,*столбец* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="0fb57-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0fb57-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fb57-107">Parameters</span></span>

  - <span data-ttu-id="0fb57-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="0fb57-108">*Key*</span></span>

  - <span data-ttu-id="0fb57-109">Объект **ключ** для добавления или имя раздела для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="0fb57-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="0fb57-110">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="0fb57-110">*KeyType*</span></span>

  - <span data-ttu-id="0fb57-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="0fb57-111">Optional.</span></span> <span data-ttu-id="0fb57-112">**Длинное** значение, задающее тип ключа.</span><span class="sxs-lookup"><span data-stu-id="0fb57-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="0fb57-113">Параметр *ключ* соответствует свойство [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) объекта **ключа** .</span><span class="sxs-lookup"><span data-stu-id="0fb57-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="0fb57-114">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="0fb57-114">*Column*</span></span>

  - <span data-ttu-id="0fb57-115">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="0fb57-115">Optional.</span></span> <span data-ttu-id="0fb57-116">**Строковое** значение, задающее имя столбца для индексирования.</span><span class="sxs-lookup"><span data-stu-id="0fb57-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="0fb57-117">Параметр *столбцы* соответствует значению свойства [Name](name-property-adox.md) объекта [столбца](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb57-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="0fb57-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="0fb57-118">*RelatedTable*</span></span>

  - <span data-ttu-id="0fb57-119">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="0fb57-119">Optional.</span></span> <span data-ttu-id="0fb57-120">**Строковое** значение, задающее имя связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="0fb57-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="0fb57-121">Параметр *RelatedTable* соответствует значению свойства **Name** объекта [в таблице](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb57-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="0fb57-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="0fb57-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="0fb57-123">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="0fb57-123">Optional.</span></span> <span data-ttu-id="0fb57-124">**Строковое** значение, задающее имя столбца, связанных с ними для внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="0fb57-124">A **String** value that specifies the name of the related column for a foreign key.</span></span> <span data-ttu-id="0fb57-125">Параметр RelatedColumn соответствует значению свойства **Name** объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="0fb57-125">The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb57-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fb57-126">Remarks</span></span>

<span data-ttu-id="0fb57-127">Для *столбцов* параметра можно задать имя столбца, либо массив имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="0fb57-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

