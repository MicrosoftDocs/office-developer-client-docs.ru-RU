---
title: PageSize Property (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480167"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="d69aa-102">PageSize Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="d69aa-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="d69aa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d69aa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d69aa-104">Указывает, сколько записей составляют одну страницу в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d69aa-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d69aa-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d69aa-105">Settings and Return Values</span></span>

<span data-ttu-id="d69aa-106">Задает или возвращает значение типа **Long** , указывающее количество записей на странице.</span><span class="sxs-lookup"><span data-stu-id="d69aa-106">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="d69aa-107">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d69aa-107">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="d69aa-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="d69aa-108">Remarks</span></span>

<span data-ttu-id="d69aa-109">Свойство **PageSize** используется для определения числа записей, входящих в состав логической страницы данных.</span><span class="sxs-lookup"><span data-stu-id="d69aa-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="d69aa-110">Создание размер страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="d69aa-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="d69aa-111">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="d69aa-111">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="d69aa-112">Это свойство можно задать в любое время и его значение будет использоваться для расчета местоположение первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="d69aa-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

