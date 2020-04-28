---
title: Метод Flush — объекты данных ActiveX (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292344"
---
# <a name="flush-method-ado"></a><span data-ttu-id="322e7-102">Метод Flush (ADO)</span><span class="sxs-lookup"><span data-stu-id="322e7-102">Flush method (ADO)</span></span>


<span data-ttu-id="322e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="322e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="322e7-104">Принудительно применяет содержимое [потока](stream-object-ado.md) , оставшееся в БУФЕРе ADO, к базовому объекту, с которым связан **поток** .</span><span class="sxs-lookup"><span data-stu-id="322e7-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="322e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="322e7-105">Syntax</span></span>

<span data-ttu-id="322e7-106">*Stream*. Удален</span><span class="sxs-lookup"><span data-stu-id="322e7-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="322e7-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="322e7-107">Remarks</span></span>

<span data-ttu-id="322e7-108">Этот метод можно использовать для отправки содержимого буфера потока в базовый объект (например, узел или файл, представленный URL-адресом, который является источником объекта **Stream** ).</span><span class="sxs-lookup"><span data-stu-id="322e7-108">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object).</span></span> <span data-ttu-id="322e7-109">Этот метод должен вызываться, когда необходимо убедиться, что все изменения, внесенные в содержимое **потока** , были записаны.</span><span class="sxs-lookup"><span data-stu-id="322e7-109">This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written.</span></span> <span data-ttu-id="322e7-110">Однако с помощью ADO обычно не требуется вызывать **flush**, так как ADO постоянно очищает буфер в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="322e7-110">However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background.</span></span> <span data-ttu-id="322e7-111">Изменения содержимого **потока** вносятся автоматически, а не кэшируются до тех пор, пока не будет вызвана **Очистка** .</span><span class="sxs-lookup"><span data-stu-id="322e7-111">Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="322e7-112">При закрытии **потока** с помощью метода [Close](close-method-ado.md) автоматически удаляется содержимое **потока** ; нет необходимости явно вызывать **Сброс** перед **закрытием**.</span><span class="sxs-lookup"><span data-stu-id="322e7-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

