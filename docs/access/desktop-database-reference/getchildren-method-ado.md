---
title: Метод GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722027"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="9937a-102">Метод GetChildren (ADO)</span><span class="sxs-lookup"><span data-stu-id="9937a-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="9937a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9937a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9937a-104">Возвращает [набор записей](recordset-object-ado.md) , строки представляют дочерние элементы коллекции [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9937a-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9937a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9937a-105">Syntax</span></span>

<span data-ttu-id="9937a-106">**Установка** *набор записей*  =  *записи*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="9937a-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="9937a-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9937a-107">Return value</span></span>

<span data-ttu-id="9937a-108">Объект **набора записей** , для которой каждая строка представляет дочернего объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="9937a-108">A **Recordset** object for which each row represents a child of the current **Record** object.</span></span> <span data-ttu-id="9937a-109">Например потомки **записи** , которая представляет каталог будет файлов и вложенных папок, содержащихся в родительской папке.</span><span class="sxs-lookup"><span data-stu-id="9937a-109">For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="9937a-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="9937a-110">Remarks</span></span>

<span data-ttu-id="9937a-111">Поставщик определяет, какие столбцы существуют в возвращаемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="9937a-111">The provider determines what columns exist in the returned **Recordset**.</span></span> <span data-ttu-id="9937a-112">Например поставщик источника документов всегда возвращает ресурсов **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="9937a-112">For example, a document source provider always returns a resource **Recordset**.</span></span>

