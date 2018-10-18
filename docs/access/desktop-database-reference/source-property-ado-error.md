---
title: Source Property (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adeadcf4c467aabad7b486bd43c12e26d67ce302
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603869"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="2eb1b-102">Source Property (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="2eb1b-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="2eb1b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2eb1b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2eb1b-104">Указывает имя объекта или приложения, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-104">Indicates the name of the object or application that originally generated an error.</span></span>

<span data-ttu-id="2eb1b-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2eb1b-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="2eb1b-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb1b-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="2eb1b-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2eb1b-107">Return value</span></span>
>>>>>>> <span data-ttu-id="2eb1b-108">master</span><span class="sxs-lookup"><span data-stu-id="2eb1b-108">master</span></span>

<span data-ttu-id="2eb1b-109">Возвращает **строковое** значение, указывающее имя объекта или приложения.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-109">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb1b-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="2eb1b-110">Remarks</span></span>

<span data-ttu-id="2eb1b-111">Используйте свойство **Source** на объект [Error](error-object-ado.md) для определения имени объекта или приложения, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-111">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="2eb1b-112">Это может быть имя класса объекта или программный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-112">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="2eb1b-113">Для ошибок в ADO будет значение свойства \**ADODB. \*\*\* имя объекта*, где *имя объекта* — это имя объекта, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-113">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="2eb1b-114">Для ADOX и ADO MD значение будет \**ADOX. \*\*\* имя объекта* и \**ADOMD. \*\*\* имя объекта,* соответственно.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-114">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="2eb1b-115">Основываясь на документацию ошибок из **источника**, [номер](number-property-ado.md)и [Описание](description-property-ado.md) свойств объектов **ошибок** , можно написать код, который будет обрабатывать ошибки соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="2eb1b-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="2eb1b-116">Свойство **Source** — только для чтения для объектов **ошибок** .</span><span class="sxs-lookup"><span data-stu-id="2eb1b-116">The **Source** property is read-only for **Error** objects.</span></span>

