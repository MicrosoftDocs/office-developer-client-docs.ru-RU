---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439802"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает текстовый поток в некомпрессованном формате с богатым текстом (RTF) из сжатого формата, используемого в **свойстве PR_RTF_COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parameters

 _lpCompressedRTFStream_
  
> [in] Указатель на поток, открытый на PR_RTF_COMPRESSED свойства сообщения. 
    
 _ulFlags_
  
> [in] Bitmask флажков параметра для функции. Можно установить следующие флаги:
    
MAPI_MODIFY 
  
> Намерен ли клиент прочитать или написать возвращенный интерфейс потоковой передачи. 
    
STORE_UNCOMPRESSED_RTF 
  
> Uncompressed RTF следует написать в поток, на который указывает  _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [вышел] Указатель на расположение, в котором **WrapCompressedRTFStream** возвращает поток для некомпрессивного RTF. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если флаг MAPI_MODIFY в параметре  _ulFlags,_ параметр  _lpCompressedRTFStream_ уже должен быть открыт для чтения и записи. В интерфейс потока, возвращаемом в  _lpUncompressedRTFStream,_ должен быть записан новый ненапечатаный текст RTF. Так как невозможно примять существующий поток, необходимо написать весь текст сообщения. 
  
Если в параметре  _ulFlags_ пройден ноль,  _lpCompressedRTFStream_ может быть открыт только для чтения. Только весь текст сообщения можно считыть из интерфейса потока, возвращенного _в lpUncompressedRTFStream._ Невозможно искать, начиная с середины потока. 
  
 **WrapCompressedRTFStream** предполагает, что указатель сжатого потока установлен в начале потока. Некоторые методы OLE **IStream** не поддерживаются возвращенным некомпрессивным потоком. К ним относятся **IStream::Clone,** **IStream::LockRegion,** **IStream::Revert,** **IStream::Seek,** **IStream::SetSize,** **IStream::Stat** и **IStream:UnlockRegion**. Для копирования всего потока необходим цикл чтения и записи. 
  
Так как клиент пишет новый RTF в некомпрессивном формате, он должен использовать **WrapCompressedRTFStream** вместо непосредственного записи в поток. Клиенты, осведомленные о RTF, должны искать флаг STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)и передать его **в WrapCompressed RTFStream,** если он установлен. 
  
## <a name="see-also"></a>См. также



[RTFSync](rtfsync.md)

