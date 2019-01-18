---
title: Добавление записей (Справочник по для настольных баз данных Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698843"
---
# <a name="adding-records"></a><span data-ttu-id="35c7f-102">Добавление записей</span><span class="sxs-lookup"><span data-stu-id="35c7f-102">Adding records</span></span>

<span data-ttu-id="35c7f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35c7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35c7f-104">Используйте метод **AddNew** для создания и инициализации новой записи в существующих **записей**.</span><span class="sxs-lookup"><span data-stu-id="35c7f-104">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**.</span></span> <span data-ttu-id="35c7f-105">Метод **поддерживает** со значением **CursorOptionEnum** **adAddNew** для проверки, является ли записи можно добавлять в текущий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="35c7f-105">You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="35c7f-106">После вызова метода **AddNew** новую запись становится текущей и остается в текущем после вызова метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="35c7f-106">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method.</span></span> <span data-ttu-id="35c7f-107">Если объект **набора записей** не поддерживает закладки, не можно получить доступ к новой записи после перемещения к другой записи.</span><span class="sxs-lookup"><span data-stu-id="35c7f-107">If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record.</span></span> <span data-ttu-id="35c7f-108">Таким образом в зависимости от типа вашей текущей позиции, может понадобиться для вызова метода **повторный запрос** для предоставления специальных возможностей новую запись.</span><span class="sxs-lookup"><span data-stu-id="35c7f-108">Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="35c7f-109">При вызове **AddNew** во время редактирования текущей записи или при добавлении новой записи, ADO вызывает метод **Update** , чтобы сохранить все изменения и затем создает новую запись.</span><span class="sxs-lookup"><span data-stu-id="35c7f-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="35c7f-110">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="35c7f-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="35c7f-111">Добавление нескольких полей</span><span class="sxs-lookup"><span data-stu-id="35c7f-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="35c7f-112">Определение режима редактирования</span><span class="sxs-lookup"><span data-stu-id="35c7f-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="35c7f-113">С помощью команды AddNew в режимах Интерпретация и пакета</span><span class="sxs-lookup"><span data-stu-id="35c7f-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

