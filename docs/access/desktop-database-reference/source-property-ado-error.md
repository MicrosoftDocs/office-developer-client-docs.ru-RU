---
title: Свойство Source (Error в ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308598"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="8c296-102">Свойство Source (Error в ADO)</span><span class="sxs-lookup"><span data-stu-id="8c296-102">Source property (ADO Error)</span></span>


<span data-ttu-id="8c296-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c296-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c296-104">Указывает имя объекта или приложения, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="8c296-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c296-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c296-105">Return value</span></span>

<span data-ttu-id="8c296-106">Возвращает **строковое** значение, которое указывает имя объекта или приложения.</span><span class="sxs-lookup"><span data-stu-id="8c296-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c296-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c296-107">Remarks</span></span>

<span data-ttu-id="8c296-108">Используйте свойство **Source** для объекта [Error](error-object-ado.md) , чтобы определить имя объекта или приложения, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="8c296-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="8c296-109">Это может быть имя класса объекта или программный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8c296-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="8c296-110">Для ошибок в ADO значение свойства равно \**ADODB. \* \* \* ObjectName*, где *objectname* — это имя объекта, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="8c296-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="8c296-111">Для ADOX и ADO MD значение будет равно \**ADOX. \* \* \* ИмяОбъекта* и \**ADOMD. \* \* \* ObjectName,* соответственно.</span><span class="sxs-lookup"><span data-stu-id="8c296-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="8c296-112">В соответствии с документацией об ошибках из свойств **Source**, [Number](number-property-ado.md)и [Description](description-property-ado.md) объектов **Error** можно написать код, который будет обрабатывать ошибку соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8c296-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="8c296-113">Свойство **Source** имеет значение только для чтения для объектов **Error** .</span><span class="sxs-lookup"><span data-stu-id="8c296-113">The **Source** property is read-only for **Error** objects.</span></span>

