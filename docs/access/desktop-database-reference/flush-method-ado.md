---
title: Метод flush — ActiveX объектов данных (ADO)
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
# <a name="flush-method-ado"></a><span data-ttu-id="99ec0-102">Метод флеша (ADO)</span><span class="sxs-lookup"><span data-stu-id="99ec0-102">Flush method (ADO)</span></span>


<span data-ttu-id="99ec0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99ec0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99ec0-104">Привнося содержимое [потока,](stream-object-ado.md) оставшегося в буфере ADO, к основному объекту, с которым связан **поток.**</span><span class="sxs-lookup"><span data-stu-id="99ec0-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ec0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99ec0-105">Syntax</span></span>

<span data-ttu-id="99ec0-106">*Stream*. Флеш</span><span class="sxs-lookup"><span data-stu-id="99ec0-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="99ec0-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="99ec0-107">Remarks</span></span>

<span data-ttu-id="99ec0-108">Этот метод может использоваться для отправки содержимого буфера потока в исходный объект (например, узел или файл, представленный URL-адресом, который является источником объекта **Stream).**</span><span class="sxs-lookup"><span data-stu-id="99ec0-108">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object).</span></span> <span data-ttu-id="99ec0-109">Этот метод должен быть вызван, если необходимо убедиться, что все изменения, внесенные в содержимое **потока,** были написаны.</span><span class="sxs-lookup"><span data-stu-id="99ec0-109">This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written.</span></span> <span data-ttu-id="99ec0-110">Однако с помощью ADO обычно не требуется вызывать **флеш,** так как ADO непрерывно сбрасывает буфер как можно больше в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="99ec0-110">However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background.</span></span> <span data-ttu-id="99ec0-111">Изменения в содержимом **Потока** вносят автоматически, а не кэшируются до тех пор, пока не будет вызван **Флеш.**</span><span class="sxs-lookup"><span data-stu-id="99ec0-111">Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="99ec0-112">Закрытие **потока** методом [Close](close-method-ado.md) автоматически смывает содержимое **потока;** нет необходимости явно вызывать флеш непосредственно **перед** **закрыть**.</span><span class="sxs-lookup"><span data-stu-id="99ec0-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

