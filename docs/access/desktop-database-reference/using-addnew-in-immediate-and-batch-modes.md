---
title: Using AddNew in Immediate and Batch Modes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312756"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="8c2dc-102">Использование AddNew в немедленных и пакетных режимах</span><span class="sxs-lookup"><span data-stu-id="8c2dc-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="8c2dc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c2dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c2dc-104">Поведение метода **AddNew** зависит от режима обновления объекта **Recordset** и от того, передаются ли аргументы *FieldList* и *Values.*</span><span class="sxs-lookup"><span data-stu-id="8c2dc-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="8c2dc-105">В режиме немедленного обновления (в котором поставщик записывает изменения в исходный источник данных после вызова метода **Update),** вызов метода **AddNew** без аргументов задает для свойства **EditMode** свойство **adEditAdd.**</span><span class="sxs-lookup"><span data-stu-id="8c2dc-105">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.**</span></span> <span data-ttu-id="8c2dc-106">Поставщик кэшетет все изменения значения поля локально.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-106">The provider caches any field value changes locally.</span></span> <span data-ttu-id="8c2dc-107">Вызов метода **Update** публикует новую запись в базе данных и сбрасывает свойство **EditMode** в **adEditNone.**</span><span class="sxs-lookup"><span data-stu-id="8c2dc-107">Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**.</span></span> <span data-ttu-id="8c2dc-108">Если передать *аргументы FieldList* и *Values,* ADO немедленно публикует новую запись в базе данных (вызов **обновления** не требуется); Значение **свойства EditMode** не меняется (**adEditNone).**</span><span class="sxs-lookup"><span data-stu-id="8c2dc-108">If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="8c2dc-109">В режиме пакетного обновления вызов метода **AddNew** без аргументов задает для свойства **EditMode** **свойство adEditAdd.**</span><span class="sxs-lookup"><span data-stu-id="8c2dc-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="8c2dc-110">Поставщик кэшетет все изменения значения поля локально.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="8c2dc-111">Вызов метода **Update** добавляет новую запись в текущий набор **recordset** и сбрасывает свойство **EditMode** в **adEditNone,** но поставщик не записи изменений в баз данных, пока вы не вызываете **метод UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="8c2dc-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="8c2dc-112">Если передать *аргументы FieldList* и *Values,* ADO отправляет новую запись поставщику для хранения в кэше; Необходимо вызвать метод **UpdateBatch,** чтобы опубликовать новую запись в базовую базу данных.</span><span class="sxs-lookup"><span data-stu-id="8c2dc-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="8c2dc-113">Дополнительные сведения об **обновлении** и **UpdateBatch** см. в главе [5 "Обновление и сохраняемая информация".](chapter-5-updating-and-persisting-data.md)</span><span class="sxs-lookup"><span data-stu-id="8c2dc-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

