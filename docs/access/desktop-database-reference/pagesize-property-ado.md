---
title: Свойство PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288135"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="8dccd-102">Свойство PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="8dccd-102">PageSize property (ADO)</span></span>


<span data-ttu-id="8dccd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dccd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8dccd-104">Указывает количество записей, составляющих одну страницу [в Наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8dccd-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8dccd-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="8dccd-105">Settings and return values</span></span>

<span data-ttu-id="8dccd-106">Задает или возвращает значение **Long,** которое указывает количество записей на странице.</span><span class="sxs-lookup"><span data-stu-id="8dccd-106">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="8dccd-107">По умолчанию используется значение 10.</span><span class="sxs-lookup"><span data-stu-id="8dccd-107">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dccd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8dccd-108">Remarks</span></span>

<span data-ttu-id="8dccd-109">Используйте **свойство PageSize,** чтобы определить, сколько записей составляют логическую страницу данных.</span><span class="sxs-lookup"><span data-stu-id="8dccd-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="8dccd-110">Установление размера страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перемещения к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="8dccd-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="8dccd-111">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю просматривать данные, просматривая определенное количество записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="8dccd-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="8dccd-112">Это свойство может быть установлено в любое время, и его значение будет использоваться для вычисления расположения первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="8dccd-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

