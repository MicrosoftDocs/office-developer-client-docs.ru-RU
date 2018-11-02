---
title: Запрашивать динамического свойства (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1898169881042b9c7af36668e26c93200d0cb5f8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924619"
---
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="86dbf-102">Запрашивать динамического свойства (ADO)</span><span class="sxs-lookup"><span data-stu-id="86dbf-102">Prompt dynamic property (ADO)</span></span>


<span data-ttu-id="86dbf-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86dbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86dbf-104">Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.</span><span class="sxs-lookup"><span data-stu-id="86dbf-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="86dbf-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="86dbf-105">Settings and return values</span></span>

<span data-ttu-id="86dbf-106">Задает и возвращает значение [ConnectPromptEnum](connectpromptenum.md) .</span><span class="sxs-lookup"><span data-stu-id="86dbf-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86dbf-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="86dbf-107">Remarks</span></span>

<span data-ttu-id="86dbf-108">**Запрос** — это динамические свойства, которое может добавляться в коллекцию [свойств](properties-collection-ado.md) объект [подключения](connection-object-ado.md) поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="86dbf-108">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider.</span></span> <span data-ttu-id="86dbf-109">Запрашивать сведения об инициализации, поставщики OLE DB обычно отображения диалогового окна для пользователя.</span><span class="sxs-lookup"><span data-stu-id="86dbf-109">To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="86dbf-110">Динамические свойства объекта [подключения](connection-object-ado.md) не сохраняются при закрытии **подключения** .</span><span class="sxs-lookup"><span data-stu-id="86dbf-110">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed.</span></span> <span data-ttu-id="86dbf-111">Свойство **приглашение** необходимо сбросить до повторного открытия **подключения** использовать значение, отличное от по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86dbf-111">The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="86dbf-112">Не указать, что поставщик должен запрашивать у пользователя в сценариях, в которых пользователь не будет отвечать на диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="86dbf-112">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box.</span></span> <span data-ttu-id="86dbf-113">Например пользователь не будет отвечать, если приложение работает на сервере системы, а не на клиенте пользователя или приложения в системе с без пользователя.</span><span class="sxs-lookup"><span data-stu-id="86dbf-113">For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on.</span></span> <span data-ttu-id="86dbf-114">В таких случаях приложение неограниченное время ожидания ответа и показаться блокировка.</span><span class="sxs-lookup"><span data-stu-id="86dbf-114">In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="86dbf-115">**Использование**</span><span class="sxs-lookup"><span data-stu-id="86dbf-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
