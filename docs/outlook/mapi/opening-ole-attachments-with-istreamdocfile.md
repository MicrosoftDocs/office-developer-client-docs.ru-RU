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
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810079"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Открытие вложения OLE с IStreamDocfile

**Применимо к**: Outlook 
  
При открытии вложения объектов OLE, с помощью интерфейса **IStreamDocfile** , а не [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** предоставляет прямой доступ к объекту с помощью структурированного хранилища, устраняя необходимость выполнения операции копирования и снизить число дополнительную нагрузку. **IStreamDocfile** — это реализации **IStream** с содержимым потока, обязательно быть в формате структурированного хранилища. **IStreamDocfile** реализуется поставщиками хранилища сообщений. 
  

