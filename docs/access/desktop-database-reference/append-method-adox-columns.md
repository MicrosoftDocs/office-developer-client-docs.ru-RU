---
title: Append Method (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480236"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="2e63f-102">Append Method (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="2e63f-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="2e63f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e63f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2e63f-104">Добавляет новый объект [столбца](column-object-adox.md) в коллекцию [столбцов](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="2e63f-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e63f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e63f-105">Syntax</span></span>

<span data-ttu-id="2e63f-106">*Столбцы*.</span><span class="sxs-lookup"><span data-stu-id="2e63f-106">*Columns*.</span></span> <span data-ttu-id="2e63f-107">Добавление*столбца* \[,*Тип* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="2e63f-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="2e63f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e63f-108">Parameters</span></span>

  - <span data-ttu-id="2e63f-109">*Столбец*</span><span class="sxs-lookup"><span data-stu-id="2e63f-109">*Column*</span></span>

  - <span data-ttu-id="2e63f-110">Объект для добавления **столбца** или имя столбца для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="2e63f-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="2e63f-111">*Тип*</span><span class="sxs-lookup"><span data-stu-id="2e63f-111">*Type*</span></span>

  - <span data-ttu-id="2e63f-112">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="2e63f-112">Optional.</span></span> <span data-ttu-id="2e63f-113">Значение типа **Long** , определяющее тип данных столбца.</span><span class="sxs-lookup"><span data-stu-id="2e63f-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="2e63f-114">Параметр *типа* соответствует свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="2e63f-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="2e63f-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="2e63f-115">*DefinedSize*</span></span>

  - <span data-ttu-id="2e63f-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="2e63f-116">Optional.</span></span> <span data-ttu-id="2e63f-117">Значение типа **Long** , определяет размер столбца.</span><span class="sxs-lookup"><span data-stu-id="2e63f-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="2e63f-118">Параметр *DefinedSize* соответствует свойству [DefinedSize](definedsize-property-adox.md) объекта **столбца** .</span><span class="sxs-lookup"><span data-stu-id="2e63f-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2e63f-119">После добавления <STRONG>столбцов</STRONG> в коллекцию <STRONG>столбцов</STRONG> <A href="index-object-adox.md">индекса</A> , если <STRONG>Столбец</STRONG> не существует в <A href="table-object-adox.md">таблице</A> , уже добавлен в коллекцию <A href="tables-collection-adox.md">таблиц</A> , произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e63f-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


