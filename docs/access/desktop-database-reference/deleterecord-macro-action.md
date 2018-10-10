---
title: DeleteRecord Macro Action
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 536369082a5abb94914d78d8bc64c5f9b45e8b0d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481999"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="32d9e-102">DeleteRecord Macro Action</span><span class="sxs-lookup"><span data-stu-id="32d9e-102">DeleteRecord Macro Action</span></span>

<span data-ttu-id="32d9e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32d9e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="32d9e-104">Чтобы удалить запись, можно использовать **УдалитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="32d9e-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="32d9e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="32d9e-105">Setting</span></span>

<span data-ttu-id="32d9e-106">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="32d9e-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32d9e-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="32d9e-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="32d9e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="32d9e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32d9e-109"><strong>Запись псевдонима</strong></span><span class="sxs-lookup"><span data-stu-id="32d9e-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="32d9e-110">Строка, идентифицирующая записи для удаления.</span><span class="sxs-lookup"><span data-stu-id="32d9e-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="32d9e-111">Если аргумент <em>псевдоним</em> не указан, текущий запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="32d9e-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="32d9e-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="32d9e-112">Remarks</span></span>

<span data-ttu-id="32d9e-113">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="32d9e-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="32d9e-114">Например используйте следующий синтаксис для ссылки на недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="32d9e-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

