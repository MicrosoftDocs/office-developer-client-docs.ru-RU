---
title: Добавление записей (Справочник по для настольных баз данных Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 760c9b2915b84457d64325c97c5118fb5debc925
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880595"
---
# <a name="adding-records"></a><span data-ttu-id="b0d2e-102">Добавление записей</span><span class="sxs-lookup"><span data-stu-id="b0d2e-102">Adding Records</span></span>


<span data-ttu-id="b0d2e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0d2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0d2e-104">Используйте метод **AddNew** для создания и инициализации новой записи в существующих **записей**.</span><span class="sxs-lookup"><span data-stu-id="b0d2e-104">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**.</span></span> <span data-ttu-id="b0d2e-105">Метод **поддерживает** со значением **CursorOptionEnum** **adAddNew** для проверки, является ли записи можно добавлять в текущий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b0d2e-105">You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="b0d2e-106">После вызова метода **AddNew** новую запись становится текущей и остается в текущем после вызова метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="b0d2e-106">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method.</span></span> <span data-ttu-id="b0d2e-107">Если объект **набора записей** не поддерживает закладки, не можно получить доступ к новой записи после перемещения к другой записи.</span><span class="sxs-lookup"><span data-stu-id="b0d2e-107">If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record.</span></span> <span data-ttu-id="b0d2e-108">Таким образом в зависимости от типа вашей текущей позиции, может понадобиться для вызова метода **повторный запрос** для предоставления специальных возможностей новую запись.</span><span class="sxs-lookup"><span data-stu-id="b0d2e-108">Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="b0d2e-109">При вызове **AddNew** во время редактирования текущей записи или при добавлении новой записи, ADO вызывает метод **Update** , чтобы сохранить все изменения и затем создает новую запись.</span><span class="sxs-lookup"><span data-stu-id="b0d2e-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="b0d2e-110">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b0d2e-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="b0d2e-111">Добавление нескольких полей</span><span class="sxs-lookup"><span data-stu-id="b0d2e-111">Adding Multiple Fields</span></span>](adding-multiple-fields.md)

- [<span data-ttu-id="b0d2e-112">Определение режима правки</span><span class="sxs-lookup"><span data-stu-id="b0d2e-112">Determining Edit Mode</span></span>](determining-edit-mode.md)

- [<span data-ttu-id="b0d2e-113">Использование метода AddNew в режиме интерпретации и пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="b0d2e-113">Using AddNew in Immediate and Batch Modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

