---
title: Свойство ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700936"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="b7636-102">Свойство ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="b7636-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="b7636-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7636-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7636-104">Указывает время ожидания при установке соединения перед завершается и генерируется ошибка.</span><span class="sxs-lookup"><span data-stu-id="b7636-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b7636-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b7636-105">Settings and return values</span></span>

<span data-ttu-id="b7636-106">Задает или возвращает значение типа **Long** , которое указывает, в секундах, время ожидания для подключения открыть.</span><span class="sxs-lookup"><span data-stu-id="b7636-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="b7636-107">Значение по умолчанию — 15.</span><span class="sxs-lookup"><span data-stu-id="b7636-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7636-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7636-108">Remarks</span></span>

<span data-ttu-id="b7636-109">Используйте свойство **ConnectionTimeout** на объект [подключения](connection-object-ado.md) Если использовать задержки сетевого трафика или высокая интенсивность операций сервера необходимо отменить попытку подключения.</span><span class="sxs-lookup"><span data-stu-id="b7636-109">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</span></span> <span data-ttu-id="b7636-110">Если перед открытием подключения истечения времени от настройки свойства **ConnectionTimeout** , возникает ошибка, и ADO отменяет попытку.</span><span class="sxs-lookup"><span data-stu-id="b7636-110">If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</span></span> <span data-ttu-id="b7636-111">Если задать свойству присваивается значение 0, ADO будет ждать неограниченное время открытия подключения.</span><span class="sxs-lookup"><span data-stu-id="b7636-111">If you set the property to zero, ADO will wait indefinitely until the connection is opened.</span></span> <span data-ttu-id="b7636-112">Убедитесь, что поставщик, к которому написании кода поддерживает функциональную возможность **ConnectionTimeout** .</span><span class="sxs-lookup"><span data-stu-id="b7636-112">Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="b7636-113">Свойство **ConnectionTimeout** — чтение и запись в случае подключения закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="b7636-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

