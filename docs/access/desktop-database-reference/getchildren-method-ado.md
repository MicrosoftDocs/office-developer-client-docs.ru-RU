---
title: Метод дочернего элемента (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292309"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="fa01a-102">Метод дочернего элемента (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa01a-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="fa01a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa01a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="fa01a-104">Возвращает объект [Recordset](recordset-object-ado.md) , в строках которого представлены дочерние элементы [записи](record-object-ado.md)коллекции.</span><span class="sxs-lookup"><span data-stu-id="fa01a-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa01a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa01a-105">Syntax</span></span>

<span data-ttu-id="fa01a-106">**Задание** *записи* *набора записей* = . GetChildren</span><span class="sxs-lookup"><span data-stu-id="fa01a-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="fa01a-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa01a-107">Return value</span></span>

<span data-ttu-id="fa01a-108">Объект **Recordset** , для которого каждая строка представляет дочерний объект текущей **записи** .</span><span class="sxs-lookup"><span data-stu-id="fa01a-108">A **Recordset** object for which each row represents a child of the current **Record** object.</span></span> <span data-ttu-id="fa01a-109">Например, дочерние элементы **записи** , представляющей каталог, будут представлять собой файлы и подкаталоги, содержащиеся в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="fa01a-109">For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa01a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa01a-110">Remarks</span></span>

<span data-ttu-id="fa01a-111">Поставщик определяет, какие столбцы существуют в возвращенном **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="fa01a-111">The provider determines what columns exist in the returned **Recordset**.</span></span> <span data-ttu-id="fa01a-112">Например, поставщик источника документов всегда возвращает **набор записей**ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa01a-112">For example, a document source provider always returns a resource **Recordset**.</span></span>

