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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает текстовый поток в несжатом формате RTF из сжатого формата, используемого в свойстве **PR_RTF_COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 
  
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

## <a name="parameters"></a>Параметры

 _lpCompressedRTFStream_
  
> [in] Указатель на поток, открытый PR_RTF_COMPRESSED свойства сообщения. 
    
 _ulFlags_
  
> [in] Битоваяmas флажков параметра для функции. Можно установить следующие флаги:
    
MAPI_MODIFY 
  
> Будет ли клиент читать или записывать возвращаемого интерфейса потока с оболочкой. 
    
STORE_UNCOMPRESSED_RTF 
  
> Несмеченный RTF должен быть записан в поток, на который указывает  _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Указатель на расположение, где **WrapCompressedRTFStream** возвращает поток для несхваченного RTF. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если флаг MAPI_MODIFY передается в  _параметре ulFlags,_ параметр  _lpCompressedRTFStream_ должен быть уже открыт для чтения и записи. Новый несмеченный текст RTF должен быть записан в интерфейс потока, возвращенный _в lpUncompressedRTFStream._ Так как невозможно примедить существующий поток, необходимо написать весь текст сообщения. 
  
Если в параметре  _ulFlags_ передается ноль,  _то lpCompressedRTFStream_ может быть открыт только для чтения. Из интерфейса потока, возвращаемого  _в lpUncompressedRTFStream,_ можно прочитать только весь текст сообщения. Поиск в середине потока невозможен. 
  
 **WrapCompressedRTFStream** предполагает, что указатель сжатого потока установлен в начале потока. Некоторые методы OLE **IStream** не поддерживаются возвращенным несмеченным потоком. К ним относятся **IStream::Clone,** **IStream::LockRegion,** **IStream::Revert,** **IStream::Seek,** **IStream::SetSize,** **IStream::Stat** и **IStream::UnlockRegion.** Для копирования во весь поток необходим цикл чтения и записи. 
  
Так как клиент записывает новый RTF в несмеченном формате, он должен использовать **WrapCompressedRTFStream** вместо прямой записи в поток. Клиенты с RTF должны искать флаг STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)и передавать его в **wrapCompressed RTFStream,** если он установлен. 
  
## <a name="see-also"></a>См. также



[RTFSync](rtfsync.md)

