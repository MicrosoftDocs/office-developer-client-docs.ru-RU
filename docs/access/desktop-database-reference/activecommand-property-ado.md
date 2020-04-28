---
title: Свойство ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281931"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="6ff79-102">Свойство ActiveCommand (ADO)</span><span class="sxs-lookup"><span data-stu-id="6ff79-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="6ff79-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ff79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ff79-104">Указывает объект [Command](command-object-ado.md) , который создал связанный объект [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff79-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ff79-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ff79-105">Return value</span></span>

<span data-ttu-id="6ff79-106">Возвращает **значение типа Variant** , которое содержит объект **Command** .</span><span class="sxs-lookup"><span data-stu-id="6ff79-106">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="6ff79-107">Значение по умолчанию — пустая ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="6ff79-107">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff79-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ff79-108">Remarks</span></span>

<span data-ttu-id="6ff79-109">Свойство **ActiveCommand** доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ff79-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="6ff79-110">Если объект **Command** не использовался для создания текущего объекта **Recordset**, возвращается ссылка на **пустой** объект.</span><span class="sxs-lookup"><span data-stu-id="6ff79-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="6ff79-111">Используйте это свойство, чтобы найти связанный объект **Command** , когда предоставляется только полученный объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="6ff79-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

