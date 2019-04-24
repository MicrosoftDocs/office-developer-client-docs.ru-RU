---
title: Динамическое свойство Prompt (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301325"
---
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="c9444-102">Динамическое свойство Prompt (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9444-102">Prompt dynamic property (ADO)</span></span>

<span data-ttu-id="c9444-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9444-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9444-104">Указывает, должен ли поставщик OLE DB запрашивать у пользователя сведения о инициализации.</span><span class="sxs-lookup"><span data-stu-id="c9444-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c9444-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c9444-105">Settings and return values</span></span>

<span data-ttu-id="c9444-106">Задает и возвращает значение [коннектпромптенум](connectpromptenum.md) .</span><span class="sxs-lookup"><span data-stu-id="c9444-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9444-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9444-107">Remarks</span></span>

<span data-ttu-id="c9444-108">**Prompt** — это динамическое свойство, которое можно добавить в коллекцию [свойств](properties-collection-ado.md) объекта [Connection](connection-object-ado.md) поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9444-108">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider.</span></span> <span data-ttu-id="c9444-109">Для получения сведений о инициализации поставщики OLE DB обычно выводят пользователю диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c9444-109">To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="c9444-110">При закрытии **подключения** теряются динамические свойства объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c9444-110">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed.</span></span> <span data-ttu-id="c9444-111">Необходимо сбросить свойство **Prompt** перед повторным открытием **подключения** , чтобы использовать значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9444-111">The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>

> [!NOTE]
> <span data-ttu-id="c9444-112">Не следует указывать, что поставщик должен запрашивать пользователя в сценариях, в которых пользователь не может ответить на диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c9444-112">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box.</span></span> <span data-ttu-id="c9444-113">Например, пользователь не сможет ответить, если приложение работает в серверной системе, а не на клиенте пользователя, или если приложение запущено в системе без входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9444-113">For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on.</span></span> <span data-ttu-id="c9444-114">В таких случаях приложение будет ждать ответа на неограниченное время и будет заблокировано.</span><span class="sxs-lookup"><span data-stu-id="c9444-114">In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span>

<span data-ttu-id="c9444-115">**Usage**</span><span class="sxs-lookup"><span data-stu-id="c9444-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
