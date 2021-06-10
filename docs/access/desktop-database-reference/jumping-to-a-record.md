---
title: Переход к записи
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290788"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="c362f-102">Переход к записи</span><span class="sxs-lookup"><span data-stu-id="c362f-102">Jumping to a record</span></span>


<span data-ttu-id="c362f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c362f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c362f-104">Метод [Move](move-method-ado.md) позволяет двигаться вперед или назад в **наборе Recordset** указанное количество записей с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c362f-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="c362f-105">Метод **Move** поддерживается во всех **объектах Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c362f-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="c362f-106">Если аргумент *NumRecords* больше нуля, текущая позиция записи перемещается вперед (ближе к концу **recordset).**</span><span class="sxs-lookup"><span data-stu-id="c362f-106">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="c362f-107">Если *значение NumRecords* меньше нуля, текущая позиция записи перемещается назад (к началу **recordset).**</span><span class="sxs-lookup"><span data-stu-id="c362f-107">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="c362f-108">Если вызов **Move** переместит текущую позицию записи в точку перед первой записью, ADO задает текущую запись позиции перед первой записью в **Recordset** **(BOF** **true).**</span><span class="sxs-lookup"><span data-stu-id="c362f-108">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**).</span></span> <span data-ttu-id="c362f-109">Попытка переместить назад, когда **свойство BOF** уже **является True,** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c362f-109">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="c362f-110">Если вызов **Move** переместит текущее положение записи в точку после последней записи, ADO задает текущую запись позиции после последней записи в **Recordset** **(EOF** является **true).**</span><span class="sxs-lookup"><span data-stu-id="c362f-110">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**).</span></span> <span data-ttu-id="c362f-111">Попытка двигаться вперед, когда **свойство EOF** уже **является True,** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c362f-111">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="c362f-112">Вызов метода **Move** из пустого объекта **Recordset** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c362f-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="c362f-113">Если вы передаете закладки в аргументе *Начните,* перемещение относительно записи с этой закладкой, если объект **Recordset** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="c362f-113">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="c362f-114">Закладка получена с помощью свойства [Bookmark.](bookmark-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c362f-114">A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property.</span></span> <span data-ttu-id="c362f-115">Если не указано, перемещение относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c362f-115">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="c362f-116">Если вы используете свойство **CacheSize** для локального кэша записей от поставщика, передав аргумент *NumRecords,* который перемещает текущую позицию записи за пределы текущей группы кэшных записей, ADO будет получать новую группу записей, начиная с записи назначения.</span><span class="sxs-lookup"><span data-stu-id="c362f-116">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="c362f-117">Свойство **CacheSize** определяет размер вновь извлеченной группы, а запись назначения — это первая извлеченная запись.</span><span class="sxs-lookup"><span data-stu-id="c362f-117">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

