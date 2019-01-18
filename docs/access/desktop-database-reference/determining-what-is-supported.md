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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712696"
---
# <a name="determining-what-is-supported"></a><span data-ttu-id="6dd02-102">Определение поддерживаемых возможностей</span><span class="sxs-lookup"><span data-stu-id="6dd02-102">Determining what is supported</span></span>

<span data-ttu-id="6dd02-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dd02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6dd02-104">Метод **поддерживает** используется для определения, поддерживает ли указанный объект **набора записей** определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="6dd02-104">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality.</span></span> <span data-ttu-id="6dd02-105">Он имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="6dd02-105">It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="6dd02-106">**Поддерживает** возвращает логическое значение, указывающее, поддерживается ли все компоненты, определяемого аргументом *CursorOptions* поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6dd02-106">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span> <span data-ttu-id="6dd02-107">Чтобы определить, какие функциональные возможности поддерживает объект **набора записей** можно использовать метод **поддерживает** .</span><span class="sxs-lookup"><span data-stu-id="6dd02-107">You can use the **Supports** method to determine what types of functionality a **Recordset** object supports.</span></span> <span data-ttu-id="6dd02-108">Если объект **набора записей** не поддерживают возможности, соответствующий константы находятся в *CursorOptions*, метод **поддерживает** возвращает **значение True**.</span><span class="sxs-lookup"><span data-stu-id="6dd02-108">If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**.</span></span> <span data-ttu-id="6dd02-109">В противном случае возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="6dd02-109">Otherwise, it returns **False**.</span></span>

<span data-ttu-id="6dd02-110">С помощью метода **поддерживает** следует проверить возможность объекта **набора записей** для добавления новых записей, используйте закладки, используйте метод **поиска** , использовать прокрутку, используйте свойство **индекса** , а также для выполнения пакета обновлений.</span><span class="sxs-lookup"><span data-stu-id="6dd02-110">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates.</span></span> <span data-ttu-id="6dd02-111">Полный список констант и их значения в разделе [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="6dd02-111">For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="6dd02-112">Несмотря на то, что метод **поддерживает** может возвращать **значение True** для указанной функции, не гарантирует, что поставщик можно включить ни при каких обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="6dd02-112">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances.</span></span> <span data-ttu-id="6dd02-113">Метод **поддерживает** просто возвращает поставщик поддерживает ли эта функция, при условии определенных условий.</span><span class="sxs-lookup"><span data-stu-id="6dd02-113">The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met.</span></span> <span data-ttu-id="6dd02-114">Например, метод **поддерживает** предупреждение может указывать, что объект **набора записей** поддерживает обновление, несмотря на то, что курсор основано на нескольких присоединиться к таблице — столбцов, некоторые из которых не подлежат обновлению.</span><span class="sxs-lookup"><span data-stu-id="6dd02-114">For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>

