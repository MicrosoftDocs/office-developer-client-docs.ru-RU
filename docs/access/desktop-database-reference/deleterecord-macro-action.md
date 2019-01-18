---
title: Макрокоманда DeleteRecord
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725954"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="a6ac0-102">Макрокоманда DeleteRecord</span><span class="sxs-lookup"><span data-stu-id="a6ac0-102">DeleteRecord macro action</span></span>

<span data-ttu-id="a6ac0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6ac0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6ac0-104">Чтобы удалить запись, можно использовать **УдалитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="a6ac0-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="a6ac0-105">Setting</span><span class="sxs-lookup"><span data-stu-id="a6ac0-105">Setting</span></span>

<span data-ttu-id="a6ac0-106">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a6ac0-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6ac0-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="a6ac0-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="a6ac0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a6ac0-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6ac0-109"><strong>Запись псевдонима</strong></span><span class="sxs-lookup"><span data-stu-id="a6ac0-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="a6ac0-110">Строка, идентифицирующая записи для удаления.</span><span class="sxs-lookup"><span data-stu-id="a6ac0-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="a6ac0-111">Если аргумент <em>псевдоним</em> не указан, текущий запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="a6ac0-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="a6ac0-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="a6ac0-112">Remarks</span></span>

<span data-ttu-id="a6ac0-113">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="a6ac0-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="a6ac0-114">Например используйте следующий синтаксис для ссылки на недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="a6ac0-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

