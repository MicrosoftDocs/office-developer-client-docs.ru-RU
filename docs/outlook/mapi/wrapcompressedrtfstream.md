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
  
Создает текстовый поток в формате несжатого текста RTF из сжатого формата, используемого в свойстве **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
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

 _лпкомпресседртфстреам_
  
> возврата Указатель на поток, Открытый в свойстве PR_RTF_COMPRESSED сообщения. 
    
 _ulFlags_
  
> возврата Битовая маска флагов Option для функции. Можно задать следующие флаги:
    
MAPI_MODIFY 
  
> Будет ли клиент намеревается считывать или записывать возвращаемый интерфейс упакованных потоков. 
    
STORE_UNCOMPRESSED_RTF 
  
> Несжатый формат RTF должен быть записан в поток, на который указывает _лпкомпресседртфстреам_
    
 _лпункомпресседртфстреам_
  
> вышли Указатель на расположение, в котором **врапкомпресседртфстреам** возвращает поток для несжатого RTF. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если флаг MAPI_MODIFY передается в параметре _ulFlags_ , параметр _лпкомпресседртфстреам_ должен быть уже открыт для чтения и записи. Новый, несжатый текст в формате RTF должен быть записан в интерфейс потока, возвращенный в _лпункомпресседртфстреам_. Так как невозможно добавить существующий поток, необходимо записать весь текст сообщения. 
  
Если в параметре _ulFlags_ передается нулевое значение, то _лпкомпресседртфстреам_ может быть открыт только для чтения. Только весь текст сообщения можно прочитать из интерфейса потока, возвращаемого в _лпункомпресседртфстреам_. Невозможно выполнить поиск, начав середину потока. 
  
 В **врапкомпресседртфстреам** предполагается, что указатель сжатого потока установлен на начало потока. Некоторые методы OLE **IStream** не поддерживаются возвращенным несжатым потоком. Сюда входят **: IStream:: Clone**, **IStream:: локкрегион**, **IStream:: revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: stat**и **IStream:: унлоккрегион**. Для копирования во весь поток необходим цикл чтения и записи. 
  
Так как клиент записывает новый формат RTF в несжатом формате, он должен использовать **врапкомпресседртфстреам**вместо прямого записи в потоке. Клиенты, поддерживающие RTF, должны выполнить поиск флага STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) и передать его в **врапкомпрессед ртфстреам** , если он задан. 
  
## <a name="see-also"></a>См. также



[RTFSync](rtfsync.md)

