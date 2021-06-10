---
title: Добавление записей (ссылка на настольные базы данных)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280289"
---
# <a name="adding-records"></a><span data-ttu-id="eabcf-102">Добавление записей</span><span class="sxs-lookup"><span data-stu-id="eabcf-102">Adding records</span></span>

<span data-ttu-id="eabcf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eabcf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eabcf-104">Используйте метод **AddNew** для создания и инициализации новой записи в существующем **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="eabcf-104">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**.</span></span> <span data-ttu-id="eabcf-105">Вы можете использовать метод **Supports** с **значением CursorOptionEnum** **adAddNew,** чтобы проверить, можно ли добавлять записи к текущему объекту **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="eabcf-105">You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="eabcf-106">После вызова метода **AddNew** новая запись становится текущей и остается текущей после вызова метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="eabcf-106">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method.</span></span> <span data-ttu-id="eabcf-107">Если объект **Recordset** не поддерживает закладки, возможно, вы не сможете получить доступ к новой записи после перемещения на другую запись.</span><span class="sxs-lookup"><span data-stu-id="eabcf-107">If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record.</span></span> <span data-ttu-id="eabcf-108">Поэтому в зависимости от типа курсора может потребоваться вызвать метод **Requery,** чтобы сделать новую запись доступной.</span><span class="sxs-lookup"><span data-stu-id="eabcf-108">Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="eabcf-109">Если вы вызываете **AddNew** при редактировании текущей записи или при добавлении новой записи, ADO вызывает метод **Update,** чтобы сохранить все изменения, а затем создает новую запись.</span><span class="sxs-lookup"><span data-stu-id="eabcf-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="eabcf-110">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="eabcf-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="eabcf-111">Добавление нескольких полей</span><span class="sxs-lookup"><span data-stu-id="eabcf-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="eabcf-112">Определение режима редактирования</span><span class="sxs-lookup"><span data-stu-id="eabcf-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="eabcf-113">Использование AddNew в режимах Immediate и Batch</span><span class="sxs-lookup"><span data-stu-id="eabcf-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

