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
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="8505c-102">Использование AddNew в неПосредственных и пакетных режимах</span><span class="sxs-lookup"><span data-stu-id="8505c-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="8505c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8505c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8505c-104">Поведение метода **AddNew** зависит от режима обновления объекта **Recordset** и от того, передаются ли аргументы *фиелдлист* и *Values* .</span><span class="sxs-lookup"><span data-stu-id="8505c-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="8505c-105">В режиме немедленного обновления (когда поставщик записывает изменения в базовом источнике данных после вызова метода **Update** ), вызов метода **AddNew** без аргументов задает для свойства **EditMode** значение **адедитадд.**</span><span class="sxs-lookup"><span data-stu-id="8505c-105">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.**</span></span> <span data-ttu-id="8505c-106">Поставщик кэширует все изменения значения поля локально.</span><span class="sxs-lookup"><span data-stu-id="8505c-106">The provider caches any field value changes locally.</span></span> <span data-ttu-id="8505c-107">Вызов метода **Update** отправляет новую запись в базу данных и сбрасывает свойство **EditMode** в **адедитноне**.</span><span class="sxs-lookup"><span data-stu-id="8505c-107">Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**.</span></span> <span data-ttu-id="8505c-108">Если вы передаете аргументы *фиелдлист* и *Values* , ADO сразу же отправляет новую запись в базу данных (вызов **обновления** не требуется); значение свойства **EditMode** не изменяется (**адедитноне**).</span><span class="sxs-lookup"><span data-stu-id="8505c-108">If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="8505c-109">В режиме пакетного обновления вызов метода **AddNew** без аргументов задает для свойства **EditMode** значение **адедитадд**.</span><span class="sxs-lookup"><span data-stu-id="8505c-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="8505c-110">Поставщик кэширует все изменения значения поля локально.</span><span class="sxs-lookup"><span data-stu-id="8505c-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="8505c-111">Вызов метода **Update** добавляет новую запись в текущий **набор записей** и сбрасывает свойство **EditMode** в **адедитноне**, но поставщик не отправляет изменения в базовую базу данных, пока не будет вызвана функция \*\*UpdateBatch \*\*метод.</span><span class="sxs-lookup"><span data-stu-id="8505c-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="8505c-112">Если вы передаете аргументы *фиелдлист* и *Values* , ADO отправляет новую запись поставщику для хранения в кэше; для отправки новой записи в базовую базу данных необходимо вызвать метод **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="8505c-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="8505c-113">Дополнительные сведения об **обновлении** и **UpdateBatch**приведены в [главе 5: обновление и постоянное обновление данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="8505c-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

