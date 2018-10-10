---
title: QueryDefStateEnum Enumeration (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68f6f1e96ae57508d94ea341b36e3a6b32cac660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481838"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="37d2b-102">QueryDefStateEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="37d2b-102">QueryDefStateEnum Enumeration (DAO)</span></span>


<span data-ttu-id="37d2b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37d2b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37d2b-104">Используется со свойством **подготовить** для указания метода используется, чтобы указать, как следует подготовить запрос.</span><span class="sxs-lookup"><span data-stu-id="37d2b-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37d2b-105">Имя</span><span class="sxs-lookup"><span data-stu-id="37d2b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="37d2b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="37d2b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="37d2b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="37d2b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37d2b-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="37d2b-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="37d2b-109">1</span><span class="sxs-lookup"><span data-stu-id="37d2b-109">1</span></span></p></td>
<td><p><span data-ttu-id="37d2b-110">(По умолчанию) Инструкция подготовлена (то есть, вызывается ODBC SQLPrepare API).</span><span class="sxs-lookup"><span data-stu-id="37d2b-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37d2b-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="37d2b-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="37d2b-112">2</span><span class="sxs-lookup"><span data-stu-id="37d2b-112">2</span></span></p></td>
<td><p><span data-ttu-id="37d2b-113">Оператор не подготовлен (то есть, вызывается ODBC SQLExecDirect API).</span><span class="sxs-lookup"><span data-stu-id="37d2b-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

