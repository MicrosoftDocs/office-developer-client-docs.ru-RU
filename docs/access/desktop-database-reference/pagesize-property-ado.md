---
title: Свойство PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883276"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="38db4-102">Свойство PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="38db4-102">PageSize property (ADO)</span></span>


<span data-ttu-id="38db4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38db4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38db4-104">Указывает, сколько записей составляют одну страницу в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="38db4-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="38db4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="38db4-105">Settings and return values</span></span>

<span data-ttu-id="38db4-106">Задает или возвращает значение типа **Long** , указывающее количество записей на странице.</span><span class="sxs-lookup"><span data-stu-id="38db4-106">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="38db4-107">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="38db4-107">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="38db4-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="38db4-108">Remarks</span></span>

<span data-ttu-id="38db4-109">Свойство **PageSize** используется для определения числа записей, входящих в состав логической страницы данных.</span><span class="sxs-lookup"><span data-stu-id="38db4-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="38db4-110">Создание размер страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="38db4-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="38db4-111">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="38db4-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="38db4-112">Это свойство можно задать в любое время и его значение будет использоваться для расчета местоположение первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="38db4-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

