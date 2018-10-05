---
title: Открытие вложения OLE с IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386553"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Открытие вложения OLE с IStreamDocfile

**Относится к**: Outlook 2013 | Outlook 2016 
  
При открытии вложения объектов OLE, с помощью интерфейса **IStreamDocfile** , а не [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** предоставляет прямой доступ к объекту с помощью структурированного хранилища, устраняя необходимость выполнения операции копирования и снизить число дополнительную нагрузку. **IStreamDocfile** — это реализации **IStream** с содержимым потока, обязательно быть в формате структурированного хранилища. **IStreamDocfile** реализуется поставщиками хранилища сообщений. 
  

