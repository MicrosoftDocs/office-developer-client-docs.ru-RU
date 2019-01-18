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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705514"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Регистрация бизнес-объектов в клиенте для использования с DCOM

**Применимо к**: Access 2013, Office 2013

Настраиваемые бизнес-объекты необходимо убедиться, что на стороне клиента можно сопоставить их имя программы (ProgId) идентификатор (класса CLSID), который может использоваться через DCOM. По этой причине программный идентификатор объекта DCOM должен быть в реестре со стороны клиента и сопоставить идентификатор класса объекта бизнеса на сервере. Для других поддерживаемых протоколов (HTTP, HTTPS и в процессе) это не требуется.

Например если предоставить объект бизнеса на сервере с именем MyBObj с Идентификатором определенного класса, например, «{00112233-4455-6677-8899-00AABBCCDDEE}», убедитесь в том, что добавлены следующие записи в реестр со стороны клиента:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

