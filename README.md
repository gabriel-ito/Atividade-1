Para fazer os quadrados de tamanhos diferentes, você pode fazer adicionando parametro, ai você escolhe os tamanhos que deseja. Uma outra forma é criar novas classes de quadrado, e alterar a variavel lado deles. E para posicioná-los em cima, é só usar flexGrow: 0.5, backgroundColor:'black', flexDirection: 'row', justifyContent: 'space-around' e width:'100%'.

Quadrado:

import React from 'react'
import {View} from 'react-native'

export default props => {
    //const lado = {}
    return (
        <View style={{height:props.lado, 
            width:props.lado, 
            backgroundColor: props.cor || '#000'}}>
        </View>
    );

}

FlexBox:

import React from 'react'
import {View,StyleSheet} from 'react-native'
import Quadrado from './Quadrado'
import Quadrado2 from './Quadrado2'
import Quadrado3 from './Quadrado3'
import Quadrado4 from './Quadrado4'
import Quadrado5 from './Quadrado5'

export default props => {
    return (
        <View style={styles.FlexV1}>
            <Quadrado lado = {20} cor=  '#7fffd4'/>
            <Quadrado lado = {25} cor= '#ff801a'/>
            <Quadrado lado = {30} cor= '#7fffd4'/>
            <Quadrado lado = {35} cor= 'pink'/>
            <Quadrado lado = {40} cor= 'blue'/>
        </View>

        
    );
}

const styles = StyleSheet.create({
    FlexV1:{       
        flexGrow: 0.5,
        backgroundColor:'black',
        flexDirection: 'row',        
        justifyContent: 'space-around',
        width:'100%'
        //flexGrow:1
    }
})
