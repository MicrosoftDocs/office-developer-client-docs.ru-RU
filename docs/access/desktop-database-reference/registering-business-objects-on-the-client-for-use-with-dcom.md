---
title: Registering Business Objects on the Client for Use with DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f3d29d20200b6e435ffafaaa35c7f507b88b939
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481394"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registering Business Objects on the Client for Use with DCOM


**Применимо к**: Access 2013 | Office 2013

Настраиваемые бизнес-объекты необходимо убедиться, что на стороне клиента можно сопоставить их имя программы (ProgId) идентификатор (класса CLSID), который может использоваться через DCOM. По этой причине программный идентификатор объекта DCOM должен быть в реестре со стороны клиента и сопоставить идентификатор класса объекта бизнеса на сервере. Для других поддерживаемых протоколов (HTTP, HTTPS и в процессе) это не требуется.

Например если предоставить объект бизнеса на сервере с именем MyBObj с Идентификатором определенного класса, например, «{00112233-4455-6677-8899-00AABBCCDDEE}», убедитесь в том, что добавлены следующие записи в реестр со стороны клиента:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

