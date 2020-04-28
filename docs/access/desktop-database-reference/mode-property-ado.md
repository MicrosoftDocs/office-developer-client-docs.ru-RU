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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288871"
---
# <a name="mode-property-ado"></a><span data-ttu-id="97382-102">Свойство Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="97382-102">Mode property (ADO)</span></span>


<span data-ttu-id="97382-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97382-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97382-104">Указывает доступные разрешения для изменения данных в объекте [подключения](connection-object-ado.md), [записи](record-object-ado.md)или [потоке](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="97382-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="97382-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="97382-105">Settings and return values</span></span>

<span data-ttu-id="97382-106">Задает или возвращает значение [коннектмодинум](connectmodeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="97382-106">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value.</span></span> <span data-ttu-id="97382-107">Значение по умолчанию для **подключения** — **адмодеункновн**.</span><span class="sxs-lookup"><span data-stu-id="97382-107">The default value for a **Connection** is **adModeUnknown**.</span></span> <span data-ttu-id="97382-108">По умолчанию для объекта **Record** задано значение **адмодереад**.</span><span class="sxs-lookup"><span data-stu-id="97382-108">The default value for a **Record** object is **adModeRead**.</span></span> <span data-ttu-id="97382-109">Значение по умолчанию для **потока** , связанного с базовым источником (открытым с URL-адресом в качестве источника, или как **поток** по умолчанию **записи**) — **адмодереад**.</span><span class="sxs-lookup"><span data-stu-id="97382-109">The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**.</span></span> <span data-ttu-id="97382-110">Значение по умолчанию для **потока** , не связанного с базовым источником (созданным в памяти), — **адмодеункновн**.</span><span class="sxs-lookup"><span data-stu-id="97382-110">The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97382-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="97382-111">Remarks</span></span>

<span data-ttu-id="97382-112">Используйте свойство **mode** , чтобы задать или вернуть разрешения на доступ, используемые поставщиком в текущем соединении.</span><span class="sxs-lookup"><span data-stu-id="97382-112">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection.</span></span> <span data-ttu-id="97382-113">Свойство **mode** можно задать только в том случае, когда объект **Connection** закрыт.</span><span class="sxs-lookup"><span data-stu-id="97382-113">You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="97382-114">Если не указан режим доступа для объекта **Stream** , он наследуется от источника, используемого для открытия объекта **Stream** .</span><span class="sxs-lookup"><span data-stu-id="97382-114">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object.</span></span> <span data-ttu-id="97382-115">Например, если **поток** открыт из объекта **Record** , по умолчанию он открывается в том же режиме, что и **запись**.</span><span class="sxs-lookup"><span data-stu-id="97382-115">For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="97382-116">Это свойство доступно для чтения и записи, а объект закрыт и доступен только для чтения, пока объект открыт.</span><span class="sxs-lookup"><span data-stu-id="97382-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="97382-117">**Использование удаленной службы данных** При использовании для объекта подключения на стороне клиента для свойства **mode** можно задать только значение **адмодеункновн**.</span><span class="sxs-lookup"><span data-stu-id="97382-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

