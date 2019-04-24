---
title: Определение поддерживаемых возможностей
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abef84f05ad279edba1fcc753f0b412a807a7b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293912"
---
# <a name="determining-what-is-supported"></a><span data-ttu-id="baa7e-102">Определение поддерживаемых возможностей</span><span class="sxs-lookup"><span data-stu-id="baa7e-102">Determining what is supported</span></span>

<span data-ttu-id="baa7e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="baa7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baa7e-104">Метод \*\*\*\* Supports используется, чтобы определить, поддерживает ли указанный объект **Recordset** определенный тип функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="baa7e-104">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality.</span></span> <span data-ttu-id="baa7e-105">Он имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="baa7e-105">It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="baa7e-106">**Поддерживает** возвращает логическое значение, которое указывает, поддерживаются ли поставщиком все компоненты, определенные аргументом *курсороптионс* .</span><span class="sxs-lookup"><span data-stu-id="baa7e-106">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span> <span data-ttu-id="baa7e-107">Можно использовать метод Supports, чтобы определить, какие типы функциональных возможностей поддерживает объект **Recordset** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="baa7e-107">You can use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="baa7e-108">Если объект **Recordset** поддерживает функции, соответствующие константы которых находятся в *курсороптионс*, метод \*\*\*\* support возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="baa7e-108">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="baa7e-109">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="baa7e-109">Otherwise, it returns **False**.</span></span>

<span data-ttu-id="baa7e-110">С помощью \*\*\*\* метода Supports можно проверить способность объекта **Recordset** добавлять новые записи, использовать закладки, использовать метод **Find** , использовать прокрутку, использовать свойство **index** и выполнять пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="baa7e-110">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates.</span></span> <span data-ttu-id="baa7e-111">Полный список констант и их значений можно найти в разделе [курсороптионенум](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="baa7e-111">For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="baa7e-112">Несмотря на \*\*\*\* то, что метод support может возвращать **значение true** для заданной функции, он не гарантирует, что поставщик может сделать эту функцию доступной во всех обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="baa7e-112">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="baa7e-113">Метод \*\*\*\* Supports просто возвращает значение, указывающее, может ли поставщик поддерживать указанные функции, при условии соблюдения определенных условий.</span><span class="sxs-lookup"><span data-stu-id="baa7e-113">The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="baa7e-114">Например, метод support \*\*\*\* может указывать на то, что объект **Recordset** поддерживает обновления, несмотря на то, что курсор основан на множественном соединении таблиц — некоторые столбцы, которые не обновляются.</span><span class="sxs-lookup"><span data-stu-id="baa7e-114">For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>

