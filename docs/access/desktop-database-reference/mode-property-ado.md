---
title: Свойство Mode (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f30dac303541b0f53d06eb7756739ff1add6ce0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712465"
---
# <a name="mode-property-ado"></a><span data-ttu-id="a2080-102">Свойство Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2080-102">Mode property (ADO)</span></span>


<span data-ttu-id="a2080-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2080-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2080-104">Указывает, доступные права на изменение данных в объекте [подключения](connection-object-ado.md), [запись](record-object-ado.md)или [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a2080-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a2080-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a2080-105">Settings and return values</span></span>

<span data-ttu-id="a2080-106">Задает или возвращает значение [ConnectModeEnum](connectmodeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="a2080-106">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value.</span></span> <span data-ttu-id="a2080-107">Значение по умолчанию для **подключения к** : **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a2080-107">The default value for a **Connection** is **adModeUnknown**.</span></span> <span data-ttu-id="a2080-108">Значение по умолчанию для объекта **записи** — **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="a2080-108">The default value for a **Record** object is **adModeRead**.</span></span> <span data-ttu-id="a2080-109">Значение по умолчанию для **потока** , связанного с базовым источником (открывается URL-адрес, как источник или **потока** **записи**по умолчанию) — **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="a2080-109">The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**.</span></span> <span data-ttu-id="a2080-110">Значение по умолчанию для **потока** , не связанные с базовым источником (создания экземпляра в памяти) — **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a2080-110">The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2080-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a2080-111">Remarks</span></span>

<span data-ttu-id="a2080-112">Используйте свойство **режима** или возвращает разрешения доступа используется поставщик в текущее подключение.</span><span class="sxs-lookup"><span data-stu-id="a2080-112">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection.</span></span> <span data-ttu-id="a2080-113">Свойство **Mode** можно задать только при закрытии объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a2080-113">You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="a2080-114">Для объекта **потока** Если режим доступа не указан, он наследуется из источника, используемого для открытия объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="a2080-114">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object.</span></span> <span data-ttu-id="a2080-115">Например если **поток** открыт из объекта **записи** , по умолчанию его открывается в том же режиме как **записи**.</span><span class="sxs-lookup"><span data-stu-id="a2080-115">For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="a2080-116">Это свойство соответствует чтения и записи, в то время как объект является закрытой и только для чтения, когда объект открыт.</span><span class="sxs-lookup"><span data-stu-id="a2080-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="a2080-117">**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **Mode** может устанавливаться только для **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a2080-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

