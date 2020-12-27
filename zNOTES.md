MY ORIGINAL ANSWER:     ColorBox.js
--------------

import React, { Component } from 'react';

export default class ColorBox extends Component {

  state = {
    todos: [
      
    ]
  }

  render() {
    
      if(this.props.opacity < 0.2) {
        return (null)
      } else {
        this.props.opacity -= 0.1
        // or =>>   this.props.opacity = this.props.opacity - 1
        return (
            <div className="color-box" style={{opacity: this.props.opacity /*replace null with the value*/}}>

                <ColorBox opacity={this.props.opacity} />
    
            </div>
        )
      }

  }

}


=====================================================

MY ORIGINAL ANSWER:     Comment.js
--------------


//your code here
import React from 'react';

class Comment extends React.Component {
    render () {

        return (
            <div className="comment">
                {this.props.commentText}
            </div>
        ) 

    }

}

export default Comment;


