---
title: Использование страниц (Справочник по для настольных баз данных Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709406"
---
# <a name="using-pages"></a><span data-ttu-id="6d9b9-102">Использование страниц</span><span class="sxs-lookup"><span data-stu-id="6d9b9-102">Using pages</span></span>


<span data-ttu-id="6d9b9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d9b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d9b9-104">Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находятся в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6d9b9-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="6d9b9-105">*Страницы* — это группы, размер которого равен значение свойства **PageSize** записей.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-105">*Pages* are groups of records whose size equals the **PageSize** property setting.</span></span> <span data-ttu-id="6d9b9-106">Даже в том случае, если последней странице не заполнен, так как меньше записей, чем значение **PageSize** , счетчиков на дополнительные в качестве значения **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="6d9b9-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="6d9b9-107">Если объекта **набора записей** не поддерживает это свойство, **PageCount** будет иметь значение -1, чтобы указать, что **PageCount** является неопределенной.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="6d9b9-108">Свойство **PageSize** используется для определения числа записей, входящих в состав логической страницы данных.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-108">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="6d9b9-109">Создание размер страницы позволяет использовать свойство **AbsolutePage** для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-109">Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page.</span></span> <span data-ttu-id="6d9b9-110">Это полезно в сценариях веб сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-110">This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="6d9b9-111">Это свойство можно задать в любое время и его значение будет использоваться для расчета местоположение первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="6d9b9-112">Свойство **AbsolutePage** используется для идентификации номер страницы, на котором расположена текущая запись.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-112">Use the **AbsolutePage** property to identify the page number on which the current record is located.</span></span> <span data-ttu-id="6d9b9-113">Опять же поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-113">Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="6d9b9-114">**AbsolutePage** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-114">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="6d9b9-115">Задайте это свойство, чтобы перейти к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="6d9b9-115">Set this property to move to the first record of a particular page.</span></span> <span data-ttu-id="6d9b9-116">Получите общее число страниц из свойства **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="6d9b9-116">Obtain the total number of pages from the **PageCount** property.</span></span>

