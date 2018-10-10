---
title: ActiveCommand Property (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482643"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="82026-102">ActiveCommand Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="82026-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="82026-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="82026-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="82026-104">Указывает объект [команды](command-object-ado.md) , которые созданы связанного объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="82026-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="82026-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82026-105">Return Value</span></span>

<span data-ttu-id="82026-106">Возвращает значение **типа Variant** , содержащее объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="82026-106">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="82026-107">Значение по умолчанию — пустая ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="82026-107">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="82026-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="82026-108">Remarks</span></span>

<span data-ttu-id="82026-109">Свойство **ActiveCommand** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82026-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="82026-110">Если объект **команды** не использовался для создания текущего **набора записей**, возвращается **значение Null,** ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="82026-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="82026-111">Это свойство используется для поиска связанного объекта **команды** , при ей предоставляется только объекте результирующего **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="82026-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

