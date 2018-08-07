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
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812627"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Относится к**: Outlook 
  
Создает текстовый поток в несжатую форматированный текст (RTF) в сжатом формате, используемые в свойстве **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Параметры

 _lpCompressedRTFStream_
  
> [in] Указатель на поток, открытый в свойстве PR_RTF_COMPRESSED сообщения. 
    
 _ulFlags_
  
> [in] Битовая маска флаги функции. Можно задать следующие флажки:
    
MAPI_MODIFY 
  
> Является ли клиентом для чтения или записи интерфейс упакованный поток, который возвращается. 
    
STORE_UNCOMPRESSED_RTF 
  
> Поток, на который указывает _lpCompressedRTFStream_ должны быть написаны несжатый формат RTF
    
 _lpUncompressedRTFStream_
  
> [out] Указатель на место, где **WrapCompressedRTFStream** возвращает поток для несжатый формат RTF. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Если флаг MAPI_MODIFY передается в параметре _ulFlags_ , параметр _lpCompressedRTFStream_ уже должен быть открыт для чтения и записи. Новый, несжатую текст RTF должны быть написаны в интерфейс потока, возвращаемого в _lpUncompressedRTFStream_. Так как не удается добавить существующего потока, должен быть написан всего текста сообщения. 
  
Ноль передается в параметре _ulFlags_ , _lpCompressedRTFStream_ может открыть, только для чтения. Поток интерфейса, возвращаемых в _lpUncompressedRTFStream_могут читать только всего текста сообщения. Начало потока в центре поиска невозможна. 
  
 **WrapCompressedRTFStream** предполагается, что указатель сжатый поток — это значение в начале потока. Некоторые методы OLE **IStream** , возвращенные несжатую потока не поддерживается. К ним относятся **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**и **IStream::UnlockRegion**. Чтобы скопировать всю потока, необходим цикл чтения и записи. 
  
Так как клиент записывает новый формат RTF в формат без сжатия, его следует использовать **WrapCompressedRTFStream**вместо непосредственно записи потока. Принять во внимание RTF клиентов следует искать флаг STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) и передайте в него **WrapCompressed RTFStream** если оно установлено. 
  
## <a name="see-also"></a>См. также



[RTFSync](rtfsync.md)

