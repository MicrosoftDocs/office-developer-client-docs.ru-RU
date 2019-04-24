---
title: RDS возвращает ошибку "Поток не прочитан"
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300856"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="54e12-102">RDS возвращает \"ошибку "поток\" не прочитан"</span><span class="sxs-lookup"><span data-stu-id="54e12-102">RDS returns \"Stream Not Read\" error</span></span>


<span data-ttu-id="54e12-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54e12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54e12-104">"Не удается прочитать объект Stream, так как он пуст или текущая позиция находится в конце потока.</span><span class="sxs-lookup"><span data-stu-id="54e12-104">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream.</span></span> <span data-ttu-id="54e12-105">Для непустых потоков задайте текущее положение с помощью свойства Position.</span><span class="sxs-lookup"><span data-stu-id="54e12-105">For non-empty Streams, set the current position with the Position property.</span></span> <span data-ttu-id="54e12-106">Чтобы определить, является ли поток пустым, проверьте свойство Size.</span><span class="sxs-lookup"><span data-stu-id="54e12-106">To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="54e12-107">Если выдается сообщение об ошибке, оно может быть результатом использования параметризованного иерархического запроса по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="54e12-107">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http.</span></span> <span data-ttu-id="54e12-108">RDS не позволяет выполнять удаленные параметризованные иерархии.</span><span class="sxs-lookup"><span data-stu-id="54e12-108">RDS does not permit you to remote parameterized hierarchies.</span></span>

