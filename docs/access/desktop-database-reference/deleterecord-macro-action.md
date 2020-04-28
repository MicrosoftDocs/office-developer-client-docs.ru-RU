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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294017"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="525f2-102">Макрокоманда DeleteRecord</span><span class="sxs-lookup"><span data-stu-id="525f2-102">DeleteRecord macro action</span></span>

<span data-ttu-id="525f2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="525f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="525f2-104">Для удаления записи можно использовать действие **DeleteRecord** .</span><span class="sxs-lookup"><span data-stu-id="525f2-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="525f2-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="525f2-105">Setting</span></span>

<span data-ttu-id="525f2-106">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="525f2-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="525f2-107">Аргументация</span><span class="sxs-lookup"><span data-stu-id="525f2-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="525f2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="525f2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="525f2-109"><strong>Псевдоним записи</strong></span><span class="sxs-lookup"><span data-stu-id="525f2-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="525f2-110">Строка, определяющая удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="525f2-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="525f2-111">Если аргумент <em>Alias</em> не указан, то текущая запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="525f2-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="525f2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="525f2-112">Remarks</span></span>

<span data-ttu-id="525f2-113">Локальную переменную **ласткреатерекордидентити** можно использовать для работы с последней записью, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="525f2-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="525f2-114">Например, используйте следующий синтаксис для ссылки на последнюю созданную запись:</span><span class="sxs-lookup"><span data-stu-id="525f2-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

