---
title: Использование страниц (Справочник по базам данных Access на компьютере)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305875"
---
# <a name="using-pages"></a><span data-ttu-id="27eac-102">Использование страниц</span><span class="sxs-lookup"><span data-stu-id="27eac-102">Using pages</span></span>


<span data-ttu-id="27eac-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27eac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27eac-104">Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находится в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="27eac-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="27eac-105">*Страницы* — это группы записей, размер которых равен значению свойства **pageSize** .</span><span class="sxs-lookup"><span data-stu-id="27eac-105">*Pages* are groups of records whose size equals the **PageSize** property setting.</span></span> <span data-ttu-id="27eac-106">Даже если последняя страница неполна, так как число записей меньше, чем значение **pageSize** , оно считается дополнительной страницей в значении **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="27eac-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="27eac-107">Если объект **Recordset** не поддерживает это свойство, **PageCount** будет иметь значение-1, указывающее на то, что **PageCount** не является детерминированным.</span><span class="sxs-lookup"><span data-stu-id="27eac-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="27eac-108">Используйте свойство **pageSize** , чтобы определить, сколько записей составляют логическую страницу данных.</span><span class="sxs-lookup"><span data-stu-id="27eac-108">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="27eac-109">Установка размера страницы позволяет использовать свойство **AbsolutePage** для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="27eac-109">Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page.</span></span> <span data-ttu-id="27eac-110">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю просматривать данные, одновременно просматривая определенное количество записей.</span><span class="sxs-lookup"><span data-stu-id="27eac-110">This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="27eac-111">Это свойство можно задать в любое время, и его значение будет использоваться для вычисления расположения первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="27eac-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="27eac-112">Используйте свойство **AbsolutePage** , чтобы определить номер страницы, на которой расположена текущая запись.</span><span class="sxs-lookup"><span data-stu-id="27eac-112">Use the **AbsolutePage** property to identify the page number on which the current record is located.</span></span> <span data-ttu-id="27eac-113">Опять же, поставщик должен поддерживать соответствующие функциональные возможности, чтобы это свойство было доступно.</span><span class="sxs-lookup"><span data-stu-id="27eac-113">Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="27eac-114">**AbsolutePage** имеет значение 1 и равняется 1, если текущая запись является первой записью в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="27eac-114">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="27eac-115">Задайте это свойство, чтобы перейти к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="27eac-115">Set this property to move to the first record of a particular page.</span></span> <span data-ttu-id="27eac-116">Получение общего числа страниц из свойства **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="27eac-116">Obtain the total number of pages from the **PageCount** property.</span></span>

