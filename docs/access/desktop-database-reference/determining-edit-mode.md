---
title: Определение режима правки
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: facad27e4579a28f45d88bfd4e440e420e70d913
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867939"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="f42d9-102">Определение режима правки</span><span class="sxs-lookup"><span data-stu-id="f42d9-102">Determining Edit Mode</span></span>


<span data-ttu-id="f42d9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f42d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f42d9-104">ADO поддерживает редактирования буфера, связанного с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f42d9-104">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="f42d9-105">Свойство **EditMode** указывает ли изменения были внесены в этот буфер или создан ли новую запись.</span><span class="sxs-lookup"><span data-stu-id="f42d9-105">The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created.</span></span> <span data-ttu-id="f42d9-106">Использование **EditMode** для определения статуса редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f42d9-106">Use **EditMode** to determine the editing status of the current record.</span></span> <span data-ttu-id="f42d9-107">Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать **обновления** или метод **CancelUpdate** .</span><span class="sxs-lookup"><span data-stu-id="f42d9-107">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="f42d9-108">**EditMode** возвращает одной из констант **EditModeEnum** , перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f42d9-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f42d9-109">Константа</span><span class="sxs-lookup"><span data-stu-id="f42d9-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="f42d9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f42d9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f42d9-111"><strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="f42d9-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="f42d9-112">Указывает, что операция редактирования не находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="f42d9-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f42d9-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="f42d9-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="f42d9-114">Указывает, что данные в текущей записи были изменены, но не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="f42d9-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f42d9-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="f42d9-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="f42d9-116">Указывает, что был вызван метод <strong>AddNew</strong> , и текущую запись в буфер копирования не новую запись, не были сохранены в базу данных.</span><span class="sxs-lookup"><span data-stu-id="f42d9-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f42d9-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="f42d9-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="f42d9-118">Указывает, что текущая запись был удален.</span><span class="sxs-lookup"><span data-stu-id="f42d9-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f42d9-119">**EditMode** можно вернуть допустимое значение только в том случае, если текущая запись.</span><span class="sxs-lookup"><span data-stu-id="f42d9-119">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="f42d9-120">**EditMode** возвращает ошибку, если \*\*справедливо **BOF** или **EOF** \*\* или текущей запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="f42d9-120">**EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

