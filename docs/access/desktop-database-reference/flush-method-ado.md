---
title: Очистка метод - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c2d7543d2e9a1229661e572e95b783621aa43fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482673"
---
# <a name="flush-method-ado"></a><span data-ttu-id="51e6f-102">Flush Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="51e6f-102">Flush Method (ADO)</span></span>


<span data-ttu-id="51e6f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="51e6f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="51e6f-104">Принудительно содержимое [потока](stream-object-ado.md) , оставшихся в буфер ADO для базового объекта, с которым связано **потока** .</span><span class="sxs-lookup"><span data-stu-id="51e6f-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e6f-105">Syntax</span></span>

<span data-ttu-id="51e6f-106">*Поток*. Очистка</span><span class="sxs-lookup"><span data-stu-id="51e6f-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="51e6f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="51e6f-107">Remarks</span></span>

<span data-ttu-id="51e6f-108">Этот метод может использоваться для отправки содержимое буфера потока базовый объект (например, узел или файл, представленный URL-адрес, который является источником объекта **потока** ).</span><span class="sxs-lookup"><span data-stu-id="51e6f-108">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object).</span></span> <span data-ttu-id="51e6f-109">Этот метод необходимо вызывать флажок, чтобы убедиться, что все изменения, внесенные в содержимое **потока** были записаны.</span><span class="sxs-lookup"><span data-stu-id="51e6f-109">This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written.</span></span> <span data-ttu-id="51e6f-110">Тем не менее с помощью ADO не обычно требуется позвонить, **Очистка**, как ADO постоянно очищает его буфер, насколько это возможно в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="51e6f-110">However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background.</span></span> <span data-ttu-id="51e6f-111">Содержимое **потока** внесения изменений автоматически, не кэшируется до **очистки** вызова.</span><span class="sxs-lookup"><span data-stu-id="51e6f-111">Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="51e6f-112">Закрытие **потока** с помощью метода [Close](close-method-ado.md) очищает содержимое **потока** автоматически. Нет необходимости явно вызывать **Очистка** непосредственно перед **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="51e6f-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

