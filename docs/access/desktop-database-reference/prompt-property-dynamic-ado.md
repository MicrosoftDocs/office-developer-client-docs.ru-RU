---
title: Prompt Property--Dynamic (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 723820a2a1c5300bfdc3e688d693d29e2bddda33
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602515"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="d81c5-102">Prompt Property--Dynamic (ADO)</span><span class="sxs-lookup"><span data-stu-id="d81c5-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="d81c5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d81c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d81c5-104">Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.</span><span class="sxs-lookup"><span data-stu-id="d81c5-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

<span data-ttu-id="d81c5-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="d81c5-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d81c5-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d81c5-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d81c5-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d81c5-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d81c5-108">master</span><span class="sxs-lookup"><span data-stu-id="d81c5-108">master</span></span>

<span data-ttu-id="d81c5-109">Задает и возвращает значение [ConnectPromptEnum](connectpromptenum.md) .</span><span class="sxs-lookup"><span data-stu-id="d81c5-109">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d81c5-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="d81c5-110">Remarks</span></span>

<span data-ttu-id="d81c5-111">**Запрос** — это динамические свойства, которое может добавляться в коллекцию [свойств](properties-collection-ado.md) объект [подключения](connection-object-ado.md) поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="d81c5-111">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider.</span></span> <span data-ttu-id="d81c5-112">Запрашивать сведения об инициализации, поставщики OLE DB обычно отображения диалогового окна для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d81c5-112">To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="d81c5-113">Динамические свойства объекта [подключения](connection-object-ado.md) не сохраняются при закрытии **подключения** .</span><span class="sxs-lookup"><span data-stu-id="d81c5-113">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed.</span></span> <span data-ttu-id="d81c5-114">Свойство **приглашение** необходимо сбросить до повторного открытия **подключения** использовать значение, отличное от по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d81c5-114">The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d81c5-115">Не указать, что поставщик должен запрашивать у пользователя в сценариях, в которых пользователь не будет отвечать на диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d81c5-115">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box.</span></span> <span data-ttu-id="d81c5-116">Например пользователь не будет отвечать, если приложение работает на сервере системы, а не на клиенте пользователя или приложения в системе с без пользователя.</span><span class="sxs-lookup"><span data-stu-id="d81c5-116">For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on.</span></span> <span data-ttu-id="d81c5-117">В таких случаях приложение неограниченное время ожидания ответа и показаться блокировка.</span><span class="sxs-lookup"><span data-stu-id="d81c5-117">In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="d81c5-118">**Использование**</span><span class="sxs-lookup"><span data-stu-id="d81c5-118">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
