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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698752"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="4e557-102">Определение режима редактирования</span><span class="sxs-lookup"><span data-stu-id="4e557-102">Determining Edit mode</span></span>


<span data-ttu-id="4e557-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e557-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e557-104">ADO поддерживает редактирования буфера, связанного с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4e557-104">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="4e557-105">Свойство **EditMode** указывает ли изменения были внесены в этот буфер или создан ли новую запись.</span><span class="sxs-lookup"><span data-stu-id="4e557-105">The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created.</span></span> <span data-ttu-id="4e557-106">Использование **EditMode** для определения статуса редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4e557-106">Use **EditMode** to determine the editing status of the current record.</span></span> <span data-ttu-id="4e557-107">Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать **обновления** или метод **CancelUpdate** .</span><span class="sxs-lookup"><span data-stu-id="4e557-107">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="4e557-108">**EditMode** возвращает одной из констант **EditModeEnum** , перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4e557-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e557-109">Константа</span><span class="sxs-lookup"><span data-stu-id="4e557-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="4e557-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4e557-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e557-111"><strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="4e557-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="4e557-112">Указывает, что операция редактирования не находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="4e557-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e557-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="4e557-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="4e557-114">Указывает, что данные в текущей записи были изменены, но не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="4e557-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e557-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="4e557-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="4e557-116">Указывает, что был вызван метод <strong>AddNew</strong> , и текущую запись в буфер копирования не новую запись, не были сохранены в базу данных.</span><span class="sxs-lookup"><span data-stu-id="4e557-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e557-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="4e557-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="4e557-118">Указывает, что текущая запись был удален.</span><span class="sxs-lookup"><span data-stu-id="4e557-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e557-119">**EditMode** можно вернуть допустимое значение только в том случае, если текущая запись.</span><span class="sxs-lookup"><span data-stu-id="4e557-119">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="4e557-120">**EditMode** возвращает ошибку, если \*\*справедливо **BOF** или **EOF** \*\* или текущей запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="4e557-120">**EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

