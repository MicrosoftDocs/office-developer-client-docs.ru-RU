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
# <a name="determining-what-is-supported"></a><span data-ttu-id="d76b5-102">Определение поддерживаемых возможностей</span><span class="sxs-lookup"><span data-stu-id="d76b5-102">Determining what is supported</span></span>

<span data-ttu-id="d76b5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d76b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d76b5-104">Метод **Supports** используется для определения того, поддерживает ли указанный объект **Recordset** определенный тип функциональности.</span><span class="sxs-lookup"><span data-stu-id="d76b5-104">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality.</span></span> <span data-ttu-id="d76b5-105">Он имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="d76b5-105">It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="d76b5-106">**Поддерживает возвращение** boolean значения, которое указывает, поддерживаются ли поставщиком все функции, указанные аргументом *CursorOptions.*</span><span class="sxs-lookup"><span data-stu-id="d76b5-106">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span> <span data-ttu-id="d76b5-107">С помощью метода **Supports** можно определить, какие типы функций поддерживает объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="d76b5-107">You can use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="d76b5-108">Если объект **Recordset поддерживает** функции, соответствующие константы которых находятся в *cursorOptions,* метод **Supports** возвращает **true**.</span><span class="sxs-lookup"><span data-stu-id="d76b5-108">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="d76b5-109">В противном случае возвращается **false.**</span><span class="sxs-lookup"><span data-stu-id="d76b5-109">Otherwise, it returns **False**.</span></span>

<span data-ttu-id="d76b5-110">С помощью метода **Supports** можно проверить возможность объекта **Recordset** добавлять новые записи, использовать закладки, использовать метод **Find,** использовать прокрутку, использовать свойство **Index** и выполнять пакетные обновления.</span><span class="sxs-lookup"><span data-stu-id="d76b5-110">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates.</span></span> <span data-ttu-id="d76b5-111">Полный список констант и их значений см. в [перечне CursorOptionEnum.](cursoroptionenum.md)</span><span class="sxs-lookup"><span data-stu-id="d76b5-111">For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="d76b5-112">Хотя метод **Supports** может возвращать **true** для заданной функции, он не гарантирует, что поставщик сможет сделать эту функцию доступной при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="d76b5-112">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="d76b5-113">Метод **Supports** просто возвращает, может ли поставщик поддерживать указанные функции при условии, что выполнены определенные условия.</span><span class="sxs-lookup"><span data-stu-id="d76b5-113">The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="d76b5-114">Например, метод **Supports** может указывать на то, что объект **Recordset** поддерживает обновления, даже если курсор основан на многостолбцах, некоторые столбцы которых невозможно обновить.</span><span class="sxs-lookup"><span data-stu-id="d76b5-114">For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>

