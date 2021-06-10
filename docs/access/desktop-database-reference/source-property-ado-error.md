---
title: Свойство Source (Error в ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061309"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="6b32f-102">Свойство Source (Error в ADO)</span><span class="sxs-lookup"><span data-stu-id="6b32f-102">Source property (ADO Error)</span></span>


<span data-ttu-id="6b32f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b32f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b32f-104">Указывает имя объекта или приложения, которые изначально создали ошибку.</span><span class="sxs-lookup"><span data-stu-id="6b32f-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b32f-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b32f-105">Return value</span></span>

<span data-ttu-id="6b32f-106">Возвращает значение **String,** которое указывает имя объекта или приложения.</span><span class="sxs-lookup"><span data-stu-id="6b32f-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b32f-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b32f-107">Remarks</span></span>

<span data-ttu-id="6b32f-108">Используйте свойство **Source** на [объекте Ошибки,](error-object-ado.md) чтобы определить имя объекта или приложения, которые изначально создали ошибку.</span><span class="sxs-lookup"><span data-stu-id="6b32f-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="6b32f-109">Это может быть имя класса объекта или программный ID.</span><span class="sxs-lookup"><span data-stu-id="6b32f-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="6b32f-110">Для ошибок в ADO значение свойства будет **ADODB.**</span><span class="sxs-lookup"><span data-stu-id="6b32f-110">For errors in ADO, the property value will be **ADODB.**</span></span> <span data-ttu-id="6b32f-111">*ObjectName,* где *ObjectName* — это имя объекта, который вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="6b32f-111">*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="6b32f-112">Для ADOX и ADO MD значение будет **ADOX.**</span><span class="sxs-lookup"><span data-stu-id="6b32f-112">For ADOX and ADO MD, the value will be **ADOX.**</span></span> <span data-ttu-id="6b32f-113">*ObjectName* и **ADOMD.**</span><span class="sxs-lookup"><span data-stu-id="6b32f-113">*ObjectName* and **ADOMD.**</span></span> <span data-ttu-id="6b32f-114">*ObjectName соответственно.*</span><span class="sxs-lookup"><span data-stu-id="6b32f-114">*ObjectName,* respectively.</span></span>

<span data-ttu-id="6b32f-115">На основе документации об ошибках из свойств **Source,** [Number](number-property-ado.md)и [Description](description-property-ado.md) объектов **Error** можно написать код, который будет соответствующим образом обрабатывать ошибку.</span><span class="sxs-lookup"><span data-stu-id="6b32f-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="6b32f-116">Свойство **Source** — только для чтения для объектов **Error.**</span><span class="sxs-lookup"><span data-stu-id="6b32f-116">The **Source** property is read-only for **Error** objects.</span></span>

