---
title: Свойство EOS (ADO - доступ к справочной базе данных настольных компьютеров))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293527"
---
# <a name="eos-property-ado"></a><span data-ttu-id="fc7d8-102">Свойство EOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc7d8-102">EOS property (ADO)</span></span>


<span data-ttu-id="fc7d8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc7d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc7d8-104">Указывает, находится ли текущая позиция в конце потока.</span><span class="sxs-lookup"><span data-stu-id="fc7d8-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="fc7d8-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fc7d8-105">Return values</span></span>

<span data-ttu-id="fc7d8-106">Возвращает значение **Boolean,** которое указывает, находится ли текущая позиция в конце потока.</span><span class="sxs-lookup"><span data-stu-id="fc7d8-106">Returns a **Boolean** value that indicates whether the current position is at the end of the stream.</span></span> <span data-ttu-id="fc7d8-107">**EOS** возвращает **True,** если в потоке больше нет bytes; возвращает **False,** если после текущей позиции больше bytes.</span><span class="sxs-lookup"><span data-stu-id="fc7d8-107">**EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="fc7d8-108">Чтобы установить конец положения потока, используйте [метод SetEOS.](seteos-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="fc7d8-108">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method.</span></span> <span data-ttu-id="fc7d8-109">Чтобы определить текущее положение, используйте свойство [Position.](position-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="fc7d8-109">To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

