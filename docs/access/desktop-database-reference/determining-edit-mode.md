---
title: Определение режима редактирования
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293919"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="be784-102">Определение режима редактирования</span><span class="sxs-lookup"><span data-stu-id="be784-102">Determining Edit mode</span></span>


<span data-ttu-id="be784-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be784-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be784-104">ADO поддерживает буфер редактирования, связанный с текущей записью.</span><span class="sxs-lookup"><span data-stu-id="be784-104">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="be784-105">Свойство **EditMode** указывает, были ли внесены изменения в этот буфер или создана ли новая запись.</span><span class="sxs-lookup"><span data-stu-id="be784-105">The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created.</span></span> <span data-ttu-id="be784-106">Используйте **EditMode** для определения состояния редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="be784-106">Use **EditMode** to determine the editing status of the current record.</span></span> <span data-ttu-id="be784-107">Вы можете проверить ожидающие изменения, если процесс редактирования был прерван, и определить, нужно ли использовать метод **Update** или **CancelUpdate.**</span><span class="sxs-lookup"><span data-stu-id="be784-107">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="be784-108">**EditMode** возвращает одну из **констант EditModeEnum,** перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="be784-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be784-109">Константа</span><span class="sxs-lookup"><span data-stu-id="be784-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="be784-110">Описание</span><span class="sxs-lookup"><span data-stu-id="be784-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be784-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="be784-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="be784-112">Указывает, что операция редактирования не идет.</span><span class="sxs-lookup"><span data-stu-id="be784-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be784-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="be784-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="be784-114">Указывает, что данные в текущей записи были изменены, но не сохранены.</span><span class="sxs-lookup"><span data-stu-id="be784-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be784-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="be784-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="be784-116">Указывает, что метод <strong>AddNew</strong> был вызван, а текущая запись в буфере копирования — это новая запись, которая не была сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="be784-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be784-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="be784-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="be784-118">Указывает, что текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="be784-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be784-119">**EditMode** может возвращать допустимые значения, только если существует текущая запись.</span><span class="sxs-lookup"><span data-stu-id="be784-119">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="be784-120">**EditMode** возвращает ошибку, если **BOF** или **EOF** имеет true или если текущая запись была удалена. </span><span class="sxs-lookup"><span data-stu-id="be784-120">**EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

