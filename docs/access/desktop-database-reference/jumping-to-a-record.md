---
title: Переход к записи
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ce27722600ae8a634092612ddf11694faa4ecef
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944475"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="53bfa-102">Переход к записи</span><span class="sxs-lookup"><span data-stu-id="53bfa-102">Jumping to a record</span></span>


<span data-ttu-id="53bfa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53bfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53bfa-104">Метод [Move](move-method-ado.md) позволяет переместить вперед или назад в **записей** указанного количества записей, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="53bfa-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="53bfa-105">Метод **Move** поддерживается для всех объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="53bfa-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="53bfa-106">Если аргумент *NumRecords* больше нуля, в настоящее время записи переход (ближе к концу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="53bfa-106">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**).</span></span> <span data-ttu-id="53bfa-107">Если *NumRecords* меньше нуля, положение текущей записи переход назад (к началу **набора записей**).</span><span class="sxs-lookup"><span data-stu-id="53bfa-107">If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="53bfa-108">Если звонок **Перемещение** перемещает положение текущей записи в точку перед первой записи, ADO задает текущую запись позицию перед первой записи в **набор записей** (**BOF** имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="53bfa-108">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**).</span></span> <span data-ttu-id="53bfa-109">При попытке выполнить переход назад, если свойство **BOF** уже имеет **значение True,** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="53bfa-109">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="53bfa-110">Если звонок **Перемещение** перемещает положение текущей записи до момента после последней записи, ADO задает текущую запись положение после последней записи в **наборе записей** (**EOF** имеет **значение True**).</span><span class="sxs-lookup"><span data-stu-id="53bfa-110">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**).</span></span> <span data-ttu-id="53bfa-111">При попытке переместить вперед в том случае, если свойство **EOF** уже имеет **значение True** приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="53bfa-111">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="53bfa-112">Вызов метода **Move** из **пустой Recordset** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="53bfa-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="53bfa-113">Если передать закладку в аргументе *Пуск* , перемещение задается запись с эту закладку, при условии, что объект **набора записей** поддерживает закладки.</span><span class="sxs-lookup"><span data-stu-id="53bfa-113">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="53bfa-114">Закладки получить с помощью свойства [Закладка](bookmark-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="53bfa-114">A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property.</span></span> <span data-ttu-id="53bfa-115">Если не указан, move — относительно текущей записи.</span><span class="sxs-lookup"><span data-stu-id="53bfa-115">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="53bfa-116">Если вы используете свойство **CacheSize** в локальный кэш записи от поставщика, передав *NumRecords* аргумент, который перемещает текущую позицию записи за пределами текущей группы кэшированной записи принудительно ADO для извлечения новую группу записей, начиная с записи назначения.</span><span class="sxs-lookup"><span data-stu-id="53bfa-116">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="53bfa-117">Свойство **CacheSize** определяет размер группы вновь извлеченных и запись назначения является первой записи извлечен.</span><span class="sxs-lookup"><span data-stu-id="53bfa-117">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

