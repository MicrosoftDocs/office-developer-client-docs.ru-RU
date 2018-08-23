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
ms.openlocfilehash: 1e11d9f663384f00e7fd867802ef63afe1dd7e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592740"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Открытие вложения OLE с IStreamDocfile

**Применимо к**: Outlook 2013 | Outlook 2016 
  
При открытии вложения объектов OLE, с помощью интерфейса **IStreamDocfile** , а не [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** предоставляет прямой доступ к объекту с помощью структурированного хранилища, устраняя необходимость выполнения операции копирования и снизить число дополнительную нагрузку. **IStreamDocfile** — это реализации **IStream** с содержимым потока, обязательно быть в формате структурированного хранилища. **IStreamDocfile** реализуется поставщиками хранилища сообщений. 
  

