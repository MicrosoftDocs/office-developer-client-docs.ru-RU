---
title: Метод GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcc687e5151e95d61939c30aa4c6be4063b67c47
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931269"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="d157c-102">Метод GetChildren (ADO)</span><span class="sxs-lookup"><span data-stu-id="d157c-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="d157c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d157c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d157c-104">Возвращает [набор записей](recordset-object-ado.md) , строки представляют дочерние элементы коллекции [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d157c-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d157c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d157c-105">Syntax</span></span>

<span data-ttu-id="d157c-106">**Установка** *набор записей*  =  *записи*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="d157c-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="d157c-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d157c-107">Return value</span></span>

<span data-ttu-id="d157c-108">Объект **набора записей** , для которой каждая строка представляет дочернего объекта **записи** .</span><span class="sxs-lookup"><span data-stu-id="d157c-108">A **Recordset** object for which each row represents a child of the current **Record** object.</span></span> <span data-ttu-id="d157c-109">Например потомки **записи** , которая представляет каталог будет файлов и вложенных папок, содержащихся в родительской папке.</span><span class="sxs-lookup"><span data-stu-id="d157c-109">For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="d157c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d157c-110">Remarks</span></span>

<span data-ttu-id="d157c-111">Поставщик определяет, какие столбцы существуют в возвращаемых **записей**.</span><span class="sxs-lookup"><span data-stu-id="d157c-111">The provider determines what columns exist in the returned **Recordset**.</span></span> <span data-ttu-id="d157c-112">Например поставщик источника документов всегда возвращает ресурсов **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d157c-112">For example, a document source provider always returns a resource **Recordset**.</span></span>

