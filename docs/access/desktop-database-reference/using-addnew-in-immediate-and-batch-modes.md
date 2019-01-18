---
title: Использование метода AddNew в режиме интерпретации и пакетном режиме
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701580"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="f797a-102">С помощью команды AddNew в режимах Интерпретация и пакета</span><span class="sxs-lookup"><span data-stu-id="f797a-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="f797a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f797a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f797a-104">Поведение метода **AddNew** зависит от режима обновления объекта **набора записей** и ли передавать аргументы *FieldList* и их *значения* .</span><span class="sxs-lookup"><span data-stu-id="f797a-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="f797a-105">В режиме немедленное обновление (где поставщик записывает изменения к базовому источнику данных после вызова метода **Update** ) вызов метода **AddNew** без аргументов присваивает свойству **EditMode** значение **adEditAdd.**</span><span class="sxs-lookup"><span data-stu-id="f797a-105">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.**</span></span> <span data-ttu-id="f797a-106">Поставщик кэширует изменения значений полей локально.</span><span class="sxs-lookup"><span data-stu-id="f797a-106">The provider caches any field value changes locally.</span></span> <span data-ttu-id="f797a-107">Вызов метода **Update** публикует новую запись в базу данных и сбрасывает свойство **EditMode** **как таковые**.</span><span class="sxs-lookup"><span data-stu-id="f797a-107">Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**.</span></span> <span data-ttu-id="f797a-108">Если передать аргументы *FieldList* и *значения* , ADO немедленно публикует новую запись в базу данных (без вызова **обновления** не требуется); значение свойства **EditMode** не изменяется (**как таковые**).</span><span class="sxs-lookup"><span data-stu-id="f797a-108">If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="f797a-109">Вызов метода **AddNew** без аргументов в пакетном режиме обновления, присваивает свойству **EditMode** **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="f797a-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="f797a-110">Поставщик кэширует изменения значений полей локально.</span><span class="sxs-lookup"><span data-stu-id="f797a-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="f797a-111">Вызов метода **Update** добавляет новую запись текущего **набора записей** и сбрасывает свойство **EditMode** **как таковые**, но поставщик не учесть изменения в основной базе данных, пока не будет вызван \*\*UpdateBatch \*\*метод.</span><span class="sxs-lookup"><span data-stu-id="f797a-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="f797a-112">Если передать аргументы *FieldList* и *значения* , ADO отправляет новую запись поставщика для хранения в кэше; необходимо вызвать метод **UpdateBatch** для публикации новой записи в основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f797a-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="f797a-113">Дополнительные сведения об **обновлении** и **UpdateBatch**можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="f797a-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

