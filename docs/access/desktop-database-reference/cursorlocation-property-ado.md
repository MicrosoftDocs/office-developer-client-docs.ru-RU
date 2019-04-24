---
title: Свойство CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295222"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="9432b-102">Свойство CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="9432b-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="9432b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9432b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9432b-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="9432b-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9432b-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9432b-105">Settings And Return Values</span></span>

<span data-ttu-id="9432b-106">Задает или возвращает значение **типа Long** , которое может быть равно одному из значений [курсорлокатионенум](cursorlocationenum.md) .</span><span class="sxs-lookup"><span data-stu-id="9432b-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9432b-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9432b-107">Remarks</span></span>

<span data-ttu-id="9432b-108">Это свойство позволяет выбирать между различными библиотеками курсоров, доступными для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9432b-108">This property allows you to choose between various cursor libraries accessible to the provider.</span></span> <span data-ttu-id="9432b-109">Как правило, можно выбрать использование клиентской библиотеки курсоров или на сервере, расположенном на сервере.</span><span class="sxs-lookup"><span data-stu-id="9432b-109">Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="9432b-110">Этот параметр свойства влияет на подключения, установленные только после задания свойства.</span><span class="sxs-lookup"><span data-stu-id="9432b-110">This property setting affects connections established only after the property has been set.</span></span> <span data-ttu-id="9432b-111">Изменение свойства **CursorLocation** не оказывает никакого действия для существующих подключений.</span><span class="sxs-lookup"><span data-stu-id="9432b-111">Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="9432b-112">Курсоры, возвращаемые методом [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) , наследуют этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9432b-112">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting.</span></span> <span data-ttu-id="9432b-113">Объекты **Recordset** будут автоматически наследовать этот параметр от связанных подключений.</span><span class="sxs-lookup"><span data-stu-id="9432b-113">**Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="9432b-114">Это свойство доступно для чтения и записи для [подключения](connection-object-ado.md) или закрытого [набора записей](recordset-object-ado.md)и доступно только для чтения в открытом **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="9432b-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="9432b-115">**Использование удаленной службы данных** При использовании в объекте **Recordset** или объекте **подключения** на стороне клиента для свойства **CursorLocation** можно задать только значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="9432b-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

