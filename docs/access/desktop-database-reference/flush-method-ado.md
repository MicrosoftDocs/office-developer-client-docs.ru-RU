---
title: Очистка метод - ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b52bb3d595c21ccc682e5af182b794065bcd1b13
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920447"
---
# <a name="flush-method-ado"></a><span data-ttu-id="45d07-102">Метод Flush (ADO)</span><span class="sxs-lookup"><span data-stu-id="45d07-102">Flush method (ADO)</span></span>


<span data-ttu-id="45d07-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45d07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45d07-104">Принудительно содержимое [потока](stream-object-ado.md) , оставшихся в буфер ADO для базового объекта, с которым связано **потока** .</span><span class="sxs-lookup"><span data-stu-id="45d07-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45d07-105">Syntax</span></span>

<span data-ttu-id="45d07-106">*Поток*. Очистка</span><span class="sxs-lookup"><span data-stu-id="45d07-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="45d07-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="45d07-107">Remarks</span></span>

<span data-ttu-id="45d07-108">Этот метод может использоваться для отправки содержимое буфера потока базовый объект (например, узел или файл, представленный URL-адрес, который является источником объекта **потока** ).</span><span class="sxs-lookup"><span data-stu-id="45d07-108">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object).</span></span> <span data-ttu-id="45d07-109">Этот метод необходимо вызывать флажок, чтобы убедиться, что все изменения, внесенные в содержимое **потока** были записаны.</span><span class="sxs-lookup"><span data-stu-id="45d07-109">This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written.</span></span> <span data-ttu-id="45d07-110">Тем не менее с помощью ADO не обычно требуется позвонить, **Очистка**, как ADO постоянно очищает его буфер, насколько это возможно в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="45d07-110">However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background.</span></span> <span data-ttu-id="45d07-111">Содержимое **потока** внесения изменений автоматически, не кэшируется до **очистки** вызова.</span><span class="sxs-lookup"><span data-stu-id="45d07-111">Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="45d07-112">Закрытие **потока** с помощью метода [Close](close-method-ado.md) очищает содержимое **потока** автоматически. Нет необходимости явно вызывать **Очистка** непосредственно перед **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="45d07-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

