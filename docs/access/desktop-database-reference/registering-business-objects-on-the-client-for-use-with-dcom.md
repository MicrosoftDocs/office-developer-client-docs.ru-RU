---
title: Регистрация бизнес-объектов в клиенте для использования с DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7479eefcc975ca0fe7bb7fe0d51796d1b1f416b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307123"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="0e0f7-102">Регистрация бизнес-объектов в клиенте для использования с DCOM</span><span class="sxs-lookup"><span data-stu-id="0e0f7-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="0e0f7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e0f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e0f7-104">Для настраиваемых бизнес-объектов необходимо убедиться, что клиент может сопоставить имя программы (ProgId) с идентификатором CLSID, который можно использовать по протоколу DCOM.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-104">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM.</span></span> <span data-ttu-id="0e0f7-105">По этой причине ProgID объекта DCOM должен находиться в реестре на стороне клиента и сопоставляться с ИДЕНТИФИКАТОРом класса серверного бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-105">For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object.</span></span> <span data-ttu-id="0e0f7-106">Для других поддерживаемых протоколов (HTTP, HTTPS и внутрипроцессный) это необязательно.</span><span class="sxs-lookup"><span data-stu-id="0e0f7-106">For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="0e0f7-107">Например, если вы предоставляли объектный бизнес-объект с именем Мибобж с определенным ИДЕНТИФИКАТОРом класса (например, "{00112233-4455-6677-8899-00AABBCCDDEE}"), убедитесь, что в реестр на стороне клиента добавлены следующие записи:</span><span class="sxs-lookup"><span data-stu-id="0e0f7-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

